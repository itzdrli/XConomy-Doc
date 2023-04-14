# 存储设置

```
Settings:
  #SQLite MySQL
  storage-type: SQLite
  #是否使用连接池
  #需要'slf4j'前置
  #至少需要JAVA11
  usepool: false
  #设置最大线程池(SQLite无此设置)
  max-threads: 5


#SQLite设置
SQLite:
  #地址为文件夹路径
  path: Default


#MySQL设置
MySQL:
  host: localhost
  port: 3306
  user: root
  pass: root
  database: data
  #自动添加 "_", 可以使用 %sign% 来表示服务器ID (见BungeeCord设置)
  table-suffix: ''
  property:
    usessl: false
    encoding: utf8
    timezone: ''
    allowPublicKeyRetrieval: false


#连接池设置
Pool-Settings:
  maximum-pool-size: 10
  minimum-idle: 10
  maximum-lifetime: 180000
  idle-timeout: 60000


#Redis设置
Redis:
  host: localhost
  port: 6379
  db-index: 1
  pool-settings:
    max-total: 10
    max-idle: 10
    min-idle: 0
  auth:
    user: ''
    pass: ''
```