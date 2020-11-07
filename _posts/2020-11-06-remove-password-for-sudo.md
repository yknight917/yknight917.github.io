---
layout: post
title: 'Ubuntu取消使用sudo命令时输入密码'
date: 2020-11-06
author: yknight
cover: 'http://on2171g4d.bkt.clouddn.com/jekyll-banner.png'
tags: ubuntu
---

### Ubuntu取消使用sudo命令时输入密码

最近收获一台全新的服务器，出于新鲜感，以及经历过不擅记录，用完即忘的痛苦，于是准备记录下对这台“新伙伴”的所有操作。



#### 编辑/etc/sudoers文件：

> sudo visudo



#### 添加以下内容：

> <username> ALL=NOPASSWD: ALL







------

官方参考：https://help.ubuntu.com/community/RootSudo

博客参考：http://www.bjhee.com/ubuntu-sudoer.html 