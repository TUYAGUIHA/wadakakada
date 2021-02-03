---
title: openvpn在mac上的使用
urlname: openvpn在mac上的使用
tags:
  - 开发工具
categories: IT
date: 2021-01-29
abbrlink: 6f6fbad6
---
## 通过修改配置文件，用以适用mac版的openVpn工具
![](/pics/21012902/2021-02-openvpn.png)
<!-- more -->
1. 下载Tunnelblick
2. 修改opvn的配置文件
3. 注释掉client.ovpn中的ip-win32 dynamic -1
4. 将三个配置文件打包成.tblk后缀名的文件
5. 在Tunnelblick中，添加该文件
6. 修改openvpn版本为：2.3.18LibreSSL
7. 点击“连接”