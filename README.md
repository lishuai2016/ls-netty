# 项目简介 （环境搭建）

这个是在https://github.com/netty/netty下载的4.1版本的zip包，在idea使用maven编译打包的时候会出现构建错误，使用去除checkstyle方式进行编译，如下:

clean package -Dmaven.test.skip=true -Dcheckstyle.skip=true

然后运行example模块的EchoServer，能正常运行不报错说明源码环境搭建成功


Netty是一个基于NIO的基于事件的高性能网络框架，在NIO里面，比较和核心的三个内容分别是Channel、Buffer、Selector，Channel负责网络数据传输，而Buffer则存储数据，Buffer可以从Channel中获取到数据，也可以向Channel里面写入数据，Selector可以监听多个Channel的事件，当发生某种事件的时候可以发出通知。

备注：【channel的作用和socket类似】


# 测试代码位置netty-example

包路径：[io.netty.example.lishuai]

比如io.netty.example.lishuai.helloworld.HelloWorldServer

- io.netty.example.lishuai
    - io            基础io
    - nio           nio
    - likeio        使用了线程池的io
    - helloworld    基于netty的测试demo





# 参考
- [ls-rpc](https://github.com/lishuai2016/lishuai-notes/tree/master/ls-rpc)
- [io\nio\aio\netty等demo](https://github.com/lishuai2016/lishuai-notes/tree/master/ls-java-core/src/main/java/com/ls/io)


# netty源码相关优秀博文

- [新手入门：目前为止最透彻的的Netty高性能原理和框架架构解析](https://www.jianshu.com/p/f16698aa8be2?utm_source=oschina-app)
- []()
- []()
- []()
- []()
- []()
- []()





