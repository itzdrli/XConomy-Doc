# 安装

>不会安装？不会汉化？本文全部教会你

## 下载

这里是一些官方的XConomy下载地址：

[SpigotMC](https://www.spigotmc.org/resources/xconomy.75669/)
[MCBBS](https://www.mcbbs.net/thread-962904-1-1.html)
[Github](https://github.com/YiC200333/XConomy/releases/)

下载之前确定你的服务端类型进行下载，Spigot/Paper/Purpur/Pufferfish/CatServer等等都需使用Bukkit版本的XConomy。

### 安装

Bukkit版请将下载下来的.jar文件复制到`/plugins`文件夹里，

Sponge为`mods`文件夹。

## 汉化

在安装后，启动一次服务端，然后关闭，接着在路径`/plugins/XConomy/`下找到配置文件`config.yml`，使用非记事本的软件打开，找到这一行：
```
Settings:
  language: English
```
将里面的`English`改为`Chinese`，然后保存，关闭；

然后删除同一目录下的文件`messages.yml`，然后启动服务器；

这时你进入服务器输入`/money`就会发现你已经成功安装并汉化了XConomy