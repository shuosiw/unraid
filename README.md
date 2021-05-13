## README

UnRaid docker 模板库，目前支持的容器：

|容器|说明|备注|
|---|---|---|
|Cloudreve|私人网盘|公私兼备，支持多家云存储驱动|
|FileBrowserEnhanced|文件管理| 灯大出品必属精品|
|IYUUPlus|自动辅种| PT 必备 |
|NFddns|动态域名解析|支持多家 DNS 的双栈解析|
|QianDao| 自动签到框架| 基于 Har，且支持推送|
|UnblockNeteaseMuisc|解锁网易云音乐灰色歌曲|Golang 版本|

原则上仅添加 UnRaid 的 APP 社区中没有提供的容器，逐步适配ing

### 使用方式

> 以添加本仓库中的 NFddns 容器实现 ipv6 的自动域名解析服务为例


#### 添加模板库

打开 unraid 的 docker 页面：

1. 将本仓库地址 https://github.com/shuosiw/unraid 填入 **Template repositories**
2. 点击 **SAVE** 保存，unraid 会自动拉取模板库并刷新页面

![添加模板库](https://raw.githubusercontent.com/shuosiw/unraid/master/.assets/add-unraid-docker-template1.jpg)


#### 添加容器

在 Unraid 自动刷新页面之后，点击 **ADD CONTAINER** 添加容器

![添加容器](https://raw.githubusercontent.com/shuosiw/unraid/master/.assets/add-unraid-docker-template2.jpg)


点击 **select a template** 展开下拉菜单，并选中 **NFddns** 容器

![添加容器](https://raw.githubusercontent.com/shuosiw/unraid/master/.assets/add-unraid-docker-template3.jpg)


#### 配置容器


选中之后会自动跳转到预设的配置页面，按照对应的要求填写配置参数：

1. 选择 alidns，并输入 AccessKey ID 以及 AccessKey Secret
2. 输入需要进行 ddns 的 IPv6 域名（不需要 IPv4 ddns 因此留空）
3. 获取方式保留默认的 public 即可

填完参数后，点击 **APPLY** 按钮应用

![添加容器](https://raw.githubusercontent.com/shuosiw/unraid/master/.assets/add-unraid-docker-template4.jpg)

> 此外还可点击 **Show more settings** 展示高级参数，比如 ddns 更新频率、域名 TTL 设置等

unraid 会自动拉取指定的镜像，并启动运行

![添加容器](https://raw.githubusercontent.com/shuosiw/unraid/master/.assets/add-unraid-docker-template5.jpg)


#### 检查确认

最后回到 UnRaid 的容器页面，可看到 NFddns 容器已处于运行中状态

![添加容器](https://raw.githubusercontent.com/shuosiw/unraid/master/.assets/add-unraid-docker-template6.jpg)

点击查看日志，可以看到已经自动渲染好配置并完成 ddns 域名解析更新，同时会每 5 分钟进行 ddns 服务。


