# enna-pushWsMessage
Use Workman to listen and send WebSocket information

原理:
1. 建立一个websocket Worker,用来维持客户端长连接
2. websocket Worker内部建立一个text Worker
3. websocket Worker与text Worker是同一个进程,可以方便的共享客户端连接
4. 某个独立的PHP后台系统通过text协议与text Worker通讯
5. text Worker操作websocket连接完成数据推送