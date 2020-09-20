# Session控制器(实现client端)

## 环境
1. jdk1.8
2. maven
3. spring cloud

## 要求
1. 根据接口描述和协议类型(见下一节)发送 session start/stop请求给服务端
2. 可支持同时(向同一个server)并发发送多个请求
3. Stop请求需要根据session 时长来发送
4. 创建日志来记录session 状态 (发送时间,发送url,和body,结果,连接信息)
5. 提供readme说明项目情况以及如何编译，运行和配置，提供编译通过的信息。

## 加分项
- 支持异步发送 ，并提供方案说明
- 支持动态调整并发参数， 
-  支持动态调整所有session时长
-  有异常处理
-  可优雅停止(比如等所有session stop后再退出)

## 运行步骤

1. 导入Maven项目
2. 运行sessionserver下的SessionserverApplication类
3. 运行sessionclient下的Main类

## 配置方法

application.properties可配置属性
* durTime 会话持续时间
* threadNum 启动的线程数
* async 是否采用异步 1:是 0:否
