# 使用 Golang 重构的 工作咩闹钟  
原项目是 [工作日闹钟](https://github.com/zanjie1999/workdayAlarmClock)，从2017年用Python2写出来后，使用Python3重构，现在使用Golang重构，最大的原因是想适配Android  

可以在每次在设定的网抑云歌单中随机抽取2首作为闹钟铃声，  
另外可以作为网抑云音乐播放器使用，随机播放永不重复，实现除语音助手外的智能音响应有的功能  

这是一个服务端程序，交互将通过8080端口的Web服务在浏览器完成，尽量减少ram占用，以便运行在骁龙210的随身WiFi上（包括Android端仅占用47M的Ram），使用蓝牙音响播放闹钟声音

这个程序将解决传统闹钟的几个问题：
1. 在节假日调休的情况下，该响的时候不响不该响的时候响
2. 闹钟铃声千篇一律，天天一样，容易听腻
3. 闹钟时间不够长，声音不够大，容易睡过头
4. 小爱音响断网后闹钟不会响
5. 闹钟随机音乐不能放我喜欢的歌
6. 随机播放重复概率过高

## 如何使用
Android使用 [App](https://github.com/zanjie1999/workdayAlarmClockAndroid)  
其他系统需要安装sox和curl，并且暂停，音量控制不可用  
Linux: `包管理器比如apt或者yum等 install sox curl`  
macOS: `brew install sox curl`  
Windows：这样启动 `workdayAlarmClock 你的播放器路径`

