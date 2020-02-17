# Asynchronous HBase

此库是基于 asynchbase next 分支修改的源码，主要是替换了 protobuf-java 包名，使得其不依赖 google 开源的 protobuf-java, 
也就不存在 protobuf-java 兼容问题

### 实现:

#### 需要了解的地方：

1. hyrule-hbase 依赖主要包含 asynchbase 和 hbase-client 两个库 
2. asynchbase 和 hbase-client 目前版本默认依赖的是 2.5.0 版本的 protobuf-java 
3. hyrule-hbase 中的 asynchbase 依赖的 protobuf-java(3.x) 存在兼容问题
4. 经过测试，hyrule-hbase 依赖的 hbase-client  兼容 protobuf-java(3.x) 版本

#### 解决兼容方法：

1. 自定义了asynchbase库(此版本不依赖 Google 的 protobuf-java)
