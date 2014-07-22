---
title: raspbian上更新apt-get镜像源
date: '2013-10-30'
layout: post
description: update raspbian system of apt-get source list
categories:
- Blog
tags:
- Raspberry Pi
---

##### 问题：
今天在raspberry pi上安装nginx，发现镜像源根本不能解析。然后更新发现也不行，发现系统默认的源已经不能解析，不是报404错误，估计有可能是被墙了。几经search终于发现一些镜像的源，具体在：[RaspbianMirrors](http://www.raspbian.org/RaspbianMirrors)。

##### 寻找源：
我选用的是：[sysu](http://mirror.sysu.edu.cn/raspbian/) ,好像是中山大学的源。

##### 更新源：

```
sudo vi /etc/apt/sources.list

```
修改地址为：

```
deb http://mirror.sysu.edu.cn/raspbian/raspbian wheezy main contrib non-free

```

更新源信息：

```
sudo apt-get update

```

下载nginx:

```
sudo apt-get install nginx

```
