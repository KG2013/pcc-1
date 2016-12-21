# pcc

[需求](https://github.com/archnotes/9courses/tree/master/PCC)

### 需求分析
* 压力所在: 每天新增的 like 对象数为 1000万，每秒计数器查询次数为 30万/秒


### 单机数据库`QPS`性能调研
???


### 架构
* 采用微服务的方式: PIG, Feed 服务，用户服务，用户行为操作服务 三个微服务
* 服务之间使用 RESTful, MQ 通信
* 当台机器 30w+ 的QPS肯定有问题，数据库需要采用分布式，主从同步


### 几个微服务以及微服务的相关表

#### PIG
Public ID Generator


#### User
* 表1 `user`
* 表2 `follower`


#### Feed
* 表1 `feed`
* 表2 `feed_action_count`


#### Action
* 表1 `action`



