# 主配置文件

```
#Default Online Offline SemiOnline
#Default模式会自动检测玩家的UUID(支持GeyserMC)
#Online模式对于开启正版验证的服务器支持更好(支持Yggdrasil)
#Offline模式不支持无视用户名大小写
UUID-mode: Default
#在转换模式下, 可以使用指令 '/xconomy' 从其他基于Vault的插件导入数据
#冲突的数据将会被跳过, 导入的数据将保存在 XConomy/importdata/data.yml
#在这个模式下，XConomy不会正常启动
#转换完成后，请进行数据检查并关闭该模式
importdata-mode: false


#设置
Settings:
  #Chinese ChineseTW English French Spanish Russian Turkish Japanese German Indonesia Portuguese
  language: Chinese
  #是否检查新版本
  check-update: true
  #TOP10和服务器总金额刷新时间间隔 (单位秒)
  refresh-time: 300
  #如果设置为true,XConomy将会注册以下指令
    # - economy
    # - eco
    # - ebalancetop
    # - ebaltop
    # - eeconomy
  #如果你服务器上有安装Essentials插件
  #XConomy将会覆盖这些指令
  eco-command: true
  #XConomy将会禁用Essentials插件的经济功能
  #仅仅是经济功能.
  disable-essentials: true
  #初始余额
  initial-bal: 0
  #pay指令需要支付的税（0.5表示50%,1表示100%）
  payment-tax: 0
  #排行榜大小 (最大值 100)
  ranking-size: 10
  #列表每页行数（排行榜以及帮助菜单）
  lines-per-page: 5
  #是否保存转账记录
  #只支持MySQL
  transaction-record: true
  #记录玩家离线期间pay指令的转账记录
  #当玩家再次上线时会收到提示
  #转账记录功能必须开启
  offline-pay-transfer-tips: false
  #无视玩家名称的大小写
  username-ignore-case: false


#非玩家账户是否启用,可以解决某些插件无法创建非玩家账户问题,比如Factions,Towny
#非玩家账户的数据不会进行BC同步
non-player-account:
  #是否启用非玩家账户
  enable: false
  #如果账户名称中包含有白名单中的字段，该账户将被识别为非玩家账户
  #否则则识别为玩家账户
  #如果玩家名称中包含有白名单中的字段, 该玩家将被拒绝进入服务器.
  #该功能可以减少从数据库读取数据的次数
  whitelist:
    #是否启用白名单
    enable: false
    fields-list:
      - town-
      - towny-
      - nation-


#货币的显示
Currency:
  singular-name: dollar
  plural-name: dollars
  #余额是否为整数
  integer-bal: false
  thousands-separator: ','
  #%format_balance% 表示格式化后的金额
  display-format: '%balance% %currencyname%'
  #最大金额 (默认为最大值)
  max-number: '10000000000000000'
  format-balance:
    10000: 万
    100000000: 亿


#BungeeCord设置
BungeeCord:
  #是否启用BC同步
  #BC同步开启后,控制台和其他插件将无法在服务器无人的情况下修改金额
  #需要在spigot.yml中设置bungeecord为true
  enable: false
  #服务器标识,请保持需要同步的子服务器的标识和数据库的设置一致
  sign: aa
```