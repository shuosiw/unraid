## 签到

<img src="https://raw.githubusercontent.com/shuosiw/unraid/master/.assets/har4.jpg" width="700">

### 说明

本目录保存了一些自己整理的 PT 站点 qiandao 全日志模板（效果如上图）：

1. 基础签到或登录：
    * 对于需要进行的签到的站点，进行签到；
    * 对于不需要进行每日签到的站点，仅访问主页（防止太久没登录 WEB 被封）
2. 获取站点的个人数据，包括：
    * 用户名
    * 上传量
    * 下载量
    * 分享率
    * 签到状态
        * 需要签到的站点会提示签到已得多少魔力
        * 不需要签到的站点则提示免签到
    * 做种数

### 全日志

这里收录的站点，均为个人调整适配过，获取对应站点全日志数据，对应模板如下：


**免签到站点**

```
站点名-免签到：【用户名:{{name}}】【魔力值:{{ml}}】【分享率:{{fx}}】【上传量:{{sc}}】【下载量:{{xz}}】【做种数:{{zz}}】
```

**签到站点**

```
站点名-签到已得{{qd}}魔力：【用户名:{{name}}】【魔力值:{{ml}}】【分享率:{{fx}}】【上传量:{{sc}}】【下载量:{{xz}}】【做种数:{{zz}}】
```

### 使用方式


> 本目录仅提供 har 文件，需要配合 [Qiandao 框架](https://github.com/shuosiw/unraid/blob/master/qiandao.xml) 使用


先找到 **我的模板**，点击 **+** 号进入 HAR 上传界面

<img src="https://raw.githubusercontent.com/shuosiw/unraid/master/.assets/har1.jpg" width="650">

找到保存在本地的 HAR 文件，选中并上传，等待上传完毕后点击 **保存** 即可

<img src="https://raw.githubusercontent.com/shuosiw/unraid/master/.assets/har2.jpg" width="650">

最后回到首页，在 **我的签到** 点击 **+** 号来创建签到任务

<img src="https://raw.githubusercontent.com/shuosiw/unraid/master/.assets/har3.jpg" width="650">

这一步就需要输入身份认证信息了，常见的有以下两种：

* cookie
* 账号密码

最后点击 **提交** 即可
