---
layout: post
title: "解决最新版 Mac OS Sierra usb网卡不能使用"
image:
  feature: abstract-10.jpg
tags: [感悟]
comments: true
share: true
published: true

---
Apple 给的解决办法:
<https://developer.apple.com/library/mac/documentation/Security/Conceptual/System_Integrity_Protection_Guide/KernelExtensions/KernelExtensions.html>


说起来很简单 ,其实就是把 mac 的新特性  一下就是解决方法
`` `System Integrity Protection` `` 关闭掉就可以了
关闭办法:

1. 重启电脑,启动时按住 Command 和 R 键;
2. 进入恢复界面后,在工具中打开 终端;
3. 输入csrutil status 查看当前状态;

`` $ csrutil status ``
``	System Integrity Protection status: enabled. ``

4. 输入: 
`` csrutil disable ``   关闭 sip 
5. 重启电脑即可


---
欢迎关注我的微信公众号**【培根的唠叨】**

![培根的唠叨](http://pic.yupoo.com/peigen123_v/FlH0GKmz/12EiFV.jpg)

---
题图： 易极付五周年活动---公司最大部门 技术中心
