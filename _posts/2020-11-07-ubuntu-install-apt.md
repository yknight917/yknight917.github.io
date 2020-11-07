---
layout: post
title: '【Ubuntu install】系列之——使用apt'
date: 2020-11-07
author: yknight
cover: 'http://on2171g4d.bkt.clouddn.com/jekyll-banner.png'
tags: ubuntu linux
---

### 【Ubuntu install】系列之——使用apt

**目录：**

- apt

- apt-get

- apt-cache

- apt-config

**apt、apt-get、apt-cache的区别：**

博客参考：https://blog.csdn.net/liudsl/article/details/79200134

博客参考：https://www.sysgeek.cn/linux-package-management/

博客参考：https://www.cnblogs.com/xwdreamer/p/3623454.html

apt:
> Debaian是Ubuntu、linux Mint和elementary OS等Linux操作系统的母版，使用的【包管理系统】为Advanced Packaging Tool（APT），注意，APT和apt命令不是指同一个东西。

> apt面向用户，适合交互使用，apt兼容部分apt-get，apt-cache，但不完全兼容

> Debian机器衍生产品的包格式为.deb，直接安装.deb包时使用dpkg命令。

**关于update**

> balabala...


#### apt

> sudo apt edit-sources

> sudo cat /etc/apt/sources.list


```
>>> apt --help

apt 1.6.12ubuntu0.1 (amd64)
Usage: apt [options] command

apt is a commandline package manager and provides commands for
searching and managing as well as querying information about packages.
It provides the same functionality as the specialized APT tools,
like apt-get and apt-cache, but enables options more suitable for
interactive use by default.

Most used commands:
  list - list packages based on package names
  search - search in package descriptions
  show - show package details
  install - install packages
  remove - remove packages
  autoremove - Remove automatically all unused packages
  update - update list of available packages
  upgrade - upgrade the system by installing/upgrading packages
  full-upgrade - upgrade the system by removing/installing/upgrading packages
  edit-sources - edit the source information file

See apt(8) for more information about the available commands.
Configuration options and syntax is detailed in apt.conf(5).
Information about how to configure sources can be found in sources.list(5).
Package and version choices can be expressed via apt_preferences(5).
Security details are available in apt-secure(8).
                                        This APT has Super Cow Powers.

```

> #### apt-get

```
>>> apt-get --help

apt 1.6.12ubuntu0.1 (amd64)
Usage: apt-get [options] command
       apt-get [options] install|remove pkg1 [pkg2 ...]
       apt-get [options] source pkg1 [pkg2 ...]

apt-get is a command line interface for retrieval of packages
and information about them from authenticated sources and
for installation, upgrade and removal of packages together
with their dependencies.

Most used commands:
  update - Retrieve new lists of packages
  upgrade - Perform an upgrade
  install - Install new packages (pkg is libc6 not libc6.deb)
  remove - Remove packages
  purge - Remove packages and config files
  autoremove - Remove automatically all unused packages
  dist-upgrade - Distribution upgrade, see apt-get(8)
  dselect-upgrade - Follow dselect selections
  build-dep - Configure build-dependencies for source packages
  clean - Erase downloaded archive files
  autoclean - Erase old downloaded archive files
  check - Verify that there are no broken dependencies
  source - Download source archives
  download - Download the binary package into the current directory
  changelog - Download and display the changelog for the given package

See apt-get(8) for more information about the available commands.
Configuration options and syntax is detailed in apt.conf(5).
Information about how to configure sources can be found in sources.list(5).
Package and version choices can be expressed via apt_preferences(5).
Security details are available in apt-secure(8).
                                        This APT has Super Cow Powers.
```

#### apt-cache

```
>>> apt-cache --help

apt 1.6.12ubuntu0.1 (amd64)
Usage: apt-cache [options] command
       apt-cache [options] show pkg1 [pkg2 ...]

apt-cache queries and displays available information about installed
and installable packages. It works exclusively on the data acquired
into the local cache via the 'update' command of e.g. apt-get. The
displayed information may therefore be outdated if the last update was
too long ago, but in exchange apt-cache works independently of the
availability of the configured sources (e.g. offline).

Most used commands:
  showsrc - Show source records
  search - Search the package list for a regex pattern
  depends - Show raw dependency information for a package
  rdepends - Show reverse dependency information for a package
  show - Show a readable record for the package
  pkgnames - List the names of all packages in the system
  policy - Show policy settings

See apt-cache(8) for more information about the available commands.
Configuration options and syntax is detailed in apt.conf(5).
Information about how to configure sources can be found in sources.list(5).
Package and version choices can be expressed via apt_preferences(5).
Security details are available in apt-secure(8).

```

> apt-config --help

```
apt 1.6.12ubuntu0.1 (amd64)
Usage: apt-config [options] command

apt-config is an interface to the configuration settings used by
all APT tools, mainly intended for debugging and shell scripting.

Most used commands:
  shell - get configuration values via shell evaluation
  dump - show the active configuration setting

See apt-config(8) for more information about the available commands.
Configuration options and syntax is detailed in apt.conf(5).
Information about how to configure sources can be found in sources.list(5).
Package and version choices can be expressed via apt_preferences(5).
Security details are available in apt-secure(8).

```