

# 目录

```

第一部分 Netty的概念及体系结构
　　第1 章 Netty——异步和事件驱动 3
　　1.1 Java 网络编程 4
　　1.1.1 Java NIO 5
　　1.1.2 选择器 6
　　1.2 Netty 简介 6
　　1.2.1 谁在使用Netty 7
　　1.2.2 异步和事件驱动 8
　　1.3 Netty 的核心组件 9
　　1.3.1 Channel 9
　　1.3.2 回调 9
　　1.3.3 Future 10
　　1.3.4 事件和ChannelHandler 11
　　1.3.5 把它们放在一起 12
　　1.4 小结 13
　　第2 章 你的第一款Netty应用程序 14
　　2.1 设置开发环境 14
　　2.1.1 获取并安装Java 开发工具包 14
　　2.1.2 下载并安装IDE 15
　　2.1.3 下载和安装Apache Maven 15
　　2.1.4 配置工具集 16
　　2.2 Netty 客户端/服务器概览 16
　　2.3 编写Echo 服务器 17
　　2.3.1 ChannelHandler 和业务逻辑 17
　　2.3.2 引导服务器 18
　　2.4 编写Echo 客户端 21
　　2.4.1 通过ChannelHandler 实现客户端逻辑 21
　　2.4.2 引导客户端 22
　　2.5 构建和运行Echo 服务器和客户端 24
　　2.5.1 运行构建 24
　　2.5.2 运行Echo 服务器和客户端 27
　　2.6 小结 29
　　第3 章 Netty 的组件和设计 30
　　3.1 Channel、EventLoop 和ChannelFuture 30
　　3.1.1 Channel 接口 31
　　3.1.2 EventLoop 接口 31
　　3.1.3 ChannelFuture 接口 32
　　3.2 ChannelHandler 和ChannelPipeline 32
　　3.2.1 ChannelHandler 接口 32
　　3.2.2 ChannelPipeline 接口 33
　　3.2.3 更加深入地了解ChannelHandler 34
　　3.2.4 编码器和解码器 35
　　3.2.5 抽象类SimpleChannelInboundHandler 35
　　3.3 引导 36
　　3.4 小结 37
　　第4 章 传输 38
　　4.1 案例研究：传输迁移 38
　　4.1.1 不通过Netty 使用OIO和NIO 39
　　4.1.2 通过Netty 使用OIO和NIO 41
　　4.1.3 非阻塞的Netty 版本 42
　　4.2 传输API 43
　　4.3 内置的传输 45
　　4.3.1 NIO——非阻塞I/O 46
　　4.3.2 Epoll——用于Linux的本地非阻塞传输 47
　　4.3.3 OIO——旧的阻塞I/O 48
　　4.3.4 用于JVM 内部通信的Local 传输 48
　　4.3.5 Embedded 传输 49
　　4.4 传输的用例 49
　　4.5 小结 51
　　第5 章 ByteBuf 52
　　5.1 ByteBuf 的API 52
　　5.2 ByteBuf 类——Netty的数据容器 53
　　5.2.1 它是如何工作的 53
　　5.2.2 ByteBuf 的使用模式 53
　　5.3 字节级操作 57
　　5.3.1 随机访问索引 57
　　5.3.2 顺序访问索引 57
　　5.3.3 可丢弃字节 58
　　5.3.4 可读字节 58
　　5.3.5 可写字节 59
　　5.3.6 索引管理 59
　　5.3.7 查找操作 60
　　5.3.8 派生缓冲区 60
　　5.3.9 读/写操作 62
　　5.3.10 更多的操作 64
　　5.4 ByteBufHolder 接口 65
　　5.5 ByteBuf 分配 65
　　5.5.1 按需分配：ByteBufAllocator 接口 65
　　5.5.2 Unpooled 缓冲区 67
　　5.5.3 ByteBufUtil 类 67
　　5.6 引用计数 67
　　5.7 小结 68
　　第6 章 ChannelHandler 和ChannelPipeline 70
　　6.1 ChannelHandler 家族 70
　　6.1.1 Channel 的生命周期 70
　　6.1.2 ChannelHandler的生命周期 71
　　6.1.3 ChannelInboundHandler接口 71
　　6.1.4 ChannelOutboundHandler接口 73
　　6.1.5 ChannelHandler 适配器 74
　　6.1.6 资源管理 74
　　6.2 ChannelPipeline 接口 76
　　6.2.1 修改ChannelPipeline 78
　　6.2.2 触发事件 79
　　6.3 ChannelHandlerContext接口 80
　　6.3.1 使用ChannelHandlerContext 82
　　6.3.2 ChannelHandler 和ChannelHandlerContext 的高级用法 84
　　6.4 异常处理 86
　　6.4.1 处理入站异常 86
　　6.4.2 处理出站异常 87
　　6.5 小结 88
　　第7 章 EventLoop 和线程模型 89
　　7.1 线程模型概述 89
　　7.2 EventLoop 接口 90
　　7.2.1 Netty 4 中的I/O 和事件处理 92
　　7.2.2 Netty 3 中的I/O 操作 92
　　7.3 任务调度 93
　　7.3.1 JDK 的任务调度API 93
　　7.3.2 使用EventLoop调度任务 94
　　7.4 实现细节 95
　　7.4.1 线程管理 95
　　7.4.2 EventLoop/线程的分配 96
　　7.5 小结 98
　　第8 章 引导 99
　　8.1 Bootstrap 类 99
　　8.2 引导客户端和无连接协议 101
　　8.2.1 引导客户端 102
　　8.2.2 Channel 和EventLoopGroup 的兼容性 103
　　8.3 引导服务器 104
　　8.3.1 ServerBootstrap 类 104
　　8.3.2 引导服务器 105
　　8.4 从Channel引导客户端 107
　　8.5 在引导过程中添加多个ChannelHandler 108
　　8.6 使用Netty 的ChannelOption 和属性 110
　　8.7 引导DatagramChannel 111
　　8.8 关闭 112
　　8.9 小结 112
　　第9 章 单元测试 113
　　9.1 EmbeddedChannel概述 113
　　9.2 使用EmbeddedChannel测试ChannelHandler 115
　　9.2.1 测试入站消息 115
　　9.2.2 测试出站消息 118
　　9.3 测试异常处理 119
　　9.4 小结 121
　　第二部分 编解码器
　　第10 章 编解码器框架 125
　　10.1 什么是编解码器 125
　　10.2 解码器 125
　　10.2.1 抽象类ByteToMessageDecoder 126
　　10.2.2 抽象类ReplayingDecoder 127
　　10.2.3 抽象类MessageToMessageDecoder 128
　　10.2.4 TooLongFrameException 类 130
　　10.3 编码器 131
　　10.3.1 抽象类MessageToByteEncoder 131
　　10.3.2 抽象类MessageToMessageEncoder 132
　　10.4 抽象的编解码器类 133
　　10.4.1 抽象类ByteToMessageCodec 133
　　10.4.2 抽象类MessageToMessageCodec 134
　　10.4.3 CombinedChannelDuplexHandler 类 137
　　10.5 小结 138
　　第11 章 预置的ChannelHandler和编解码器 139
　　11.1 通过SSL/TLS 保护Netty 应用程序 139
　　11.2 构建基于Netty 的HTTP/HTTPS 应用程序 141
　　11.2.1 HTTP 解码器、编码器和编解码器 141
　　11.2.2 聚合HTTP 消息 143
　　11.2.3 HTTP 压缩 144
　　11.2.4 使用HTTPS 145
　　11.2.5 WebSocket 146
　　11.3 空闲的连接和超时 148
　　11.4 解码基于分隔符的协议和基于长度的协议 150
　　11.4.1 基于分隔符的协议 150
　　11.4.2 基于长度的协议 153
　　11.5 写大型数据 155
　　11.6 序列化数据 1 57
　　11.6.1 JDK 序列化 157
　　11.6.2 使用JBoss Marshalling进行序列化 157
　　11.6.3 通过Protocol Buffers序列化 159
　　11.7 小结 160
　　第三部分 网络协议
　　第12 章 WebSocket 163
　　12.1 WebSocket 简介 163
　　12.2 我们的WebSocket 示例应用程序 164
　　12.3 添加WebSocket支持 165
　　12.3.1 处理HTTP 请求 165
　　12.3.2 处理WebSocket 帧 168
　　12.3.3 初始化ChannelPipeline 169
　　12.3.4 引导 171
　　12.4 测试该应用程序 173
　　12.5 小结 176
　　第13章 使用UDP 广播事件 177
　　13.1 UDP 的基础知识 177
　　13.2 UDP 广播 178
　　13.3 UDP 示例应用程序 178
　　13.4 消息 POJO:LogEvent 179
　　13.5 编写广播者 180
　　13.6 编写监视器 185
　　13.7 运行LogEventBroadcaster 和LogEventMonitor 187
　　13.8 小结 189
　　第四部分 案例研究
　　第14 章 案例研究，第一部分 193
　　14.1 Droplr—构建移动服务 193
　　14.1.1 这一切的起因 193
　　14.1.2 Droplr 是怎样工作的 194
　　14.1.3 创造一个更加快速的上传体验 194
　　14.1.4 技术栈 196
　　14.1.5 性能 199
　　14.1.6 小结——站在巨人的肩膀上 200
　　14.2 Firebase—实时的数据同步服务 200
　　14.2.1 Firebase 的架构 201
　　14.2.2 长轮询 201
　　14.2.3 HTTP 1.1 keep-alive和流水线化 204
　　14.2.4 控制SslHandler 205
　　14.2.5 Firebase 小结 207
　　14.3 Urban Airship—构建移动服务 207
　　14.3.1 移动消息的基础知识 207
　　14.3.2 第三方递交 208
　　14.3.3 使用二进制协议的例子 209
　　14.3.4 直接面向设备的递交 211
　　14.3.5 Netty 擅长管理大量的并发连接 212
　　14.3.6 Urban Airship 小结——跨越防火墙边界 213
　　14.4 小结 214
　　第15 章 案例研究，第二部分 215
　　15.1 Netty 在Facebook 的使用：Nifty 和Swift 215
　　15.1.1 什么是Thrift 215
　　15.1.2 使用Netty 改善Java Thrift 的现状 216
　　15.1.3 Nifty 服务器的设计 217
　　15.1.4 Nifty 异步客户端的设计 220
　　15.1.5 Swift：一种更快的构建Java Thrift 服务的方式 221
　　15.1.6 结果 221
　　15.1.7 Facebook 小结 224
　　15.2 Netty 在Twitter的使用：Finagle 224
　　15.2.1 Twitter 成长的烦恼 224
　　15.2.2 Finagle 的诞生 224
　　15.2.3 Finagle 是如何工作的 225
　　15.2.4 Finagle 的抽象 230
　　15.2.5 故障管理 231
　　15.2.6 组合服务 232
　　15.2.7 未来：Netty 232
　　15.2.8 Twitter 小结 233
　　15.3 小结 233
　　附录 Maven 介绍 234 [1] 


```