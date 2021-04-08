# DHT-network DHT 网络， 分布式去中心化存储技术学习
ipfs web3.0的愿景 我们来探讨一下DHT网络

## 我们先来探讨下 有那些存储架构
### 中心化存储
FTP文件服务器，最近比较火的NAS  将数据集中存储在一点上
- 优点
    * 架设简单
- 缺点
    * 中心节点故障 整个网络瘫痪 数据丢失
    * 所有访问量集中于一点 考验软硬及其网络承受能力

### BitTorrent-tracker
中心服务器Tracker 保存各个节点地址信息, 下载节点查询Tracker获取存储节点信息

就有点像现在流行的微服务, 注册中心挂掉整个系统瘫痪

- 缺点
    - 过于依赖Tracker  

### BitTorrent-DHT
#### 前置知识
- peer: 实现BT协议 并开启TCP监听端口的BT 客户端 或 服务端
- node: 实现DHT协议 并开启UDP监听端口的BT 客户端 或 服务端
- tracker: 索引服务器, 指引资源所在peer. DHT网络中 存储peer信息的node节点作为虚拟tracker
- info_hash: 资源唯一标识符

