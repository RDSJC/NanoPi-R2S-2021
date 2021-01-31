# r2s固件，每天自动编译最新插件和内核。

## 目前的编译已修复卡刷无法开机的问题。

我的固件很挑卡。不过目前已解决了卡刷不开机的问题。

方法两种：

- 下载r4s固件刷到卡上，然后再刷r2s即可解决挑卡问题，就能开机

- 用软件卡写到一半就拔出，再写卡完了即可清除分区里的垃圾。（感谢Aney提供）

 以上这两种方法即可解决挑卡不开机问题！

 还有一件事 我的固件加了动态超频，不管热不热这是取决后台运行程序在跑什么。
 
 
 感觉很热  就加风扇，推荐 风扇6cm×6cm，薄1cm，usb也行 或者端子线zh1.5
  
### 默认编译

- 用户名：root 密码：password 管理IP：192.168.2.1

# 离线升级

## 需要的软件
WinScp 下载链接 https://wws.lanzous.com/ivi2ql56mod

# 请将需要使用的固件只支持squashfs固件格式，是ext4格式请不要使用此方法（img格式，不是压缩包！压缩包请先解压成img）存在本地你记得住的一个文件夹

首先，打开WinScp。登陆教程自己~~百度~~谷歌，懂？

切换到 /tmp 文件夹。在左边选择img镜像所在路径，拖到tmp文件夹里面。

等待复制完成，就点...返回根目录。

在这里，按下快捷键Shift+Ctrl+T，输入以下代码。

注意，<>内的内容请根据img文件名自行修改

```
sysupgrade tmp/<你的文件名>.img
```

点击执行，稍等几秒会出现一个弹窗。在弹窗中，选择确定。

现在，你可以泡一杯咖啡，等大概三分钟，更新就完成了。而且，与以往不同，你的配置在新固件内会被保留，所以基本不需要设置了。但是，我还是建议你检查一下配置，以防万一。

如果出现各种奇奇怪怪的问题，那么我还是劝你重新卡刷，耗子尾汁，不要搞窝里斗。
 
### (离线升级由[thomaswcy](https://github.com/thomaswcy/op-direct-upgrade "thomaswcy")提供，非常感谢！)

## 更新日志1.30号

- 增新了ipv6客户端，快速获取ipv6

- 修复了ipv6情况下节点有时断开，提高上网质量；

- 增加了helloworld插件

- 修复了adguardhome插件无法启动问题，改为Lienol源码仓库的插件

## 后续再说
