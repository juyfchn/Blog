---
layout: post
title:  "Easy-V2ray一键完成V2ray安装并生成配置文件"
date:   2017-08-01 13:46:40
categories: Skill
---
## 简介 ##

V2ray是一个模块化的代理程序，类似于SS。但是其诞生之初就是为了解决部分SS的缺点以及增加一些特色的改良功能。由于起模块化的设计，功能十分强大，但是配置文件这一步难倒了不少小白。本人在网上收集大量教程整合并修改完成了这个一键包（感谢雨落无声提供的源码），帮助大家快速上手V2ray，体验体验~ 具体功能可以参考官方网站：[v2ray.com][1]

## 脚本 ##

Github地址：
[https://github.com/Moexin/Easy-V2ray][2]

**功能**

 - 利用官方脚本部署V2ray,简单方便
 - 一键生成服务器和客户端配置，不再为配置文件而烦恼
 - 支持选择mkcp协议 (https://www.v2ray.com/chapter_03/kcp.html)
 - 支持开启http头部伪装 (https://toutyrater.github.io/v2ray-guide-pages/advance_config/httpfake.html)
 - 全中文提示，可一路回车完成配置
 - 自动绕过大陆常用域名和大陆地区IP地址，只加速海外流量。(https://www.v2ray.com/chapter_02/03_routing.html)
 - 可选择开启动态端口功能。（https://toutyrater.github.io/v2ray-guide-pages/advance_config/dynamicport.html）
 - 可选择客户端是socks代理或者是http代理
 - 可选择开启 Mux.Cool
 - 默认开启UDP支持

**提醒**

 - 可以反复运行此脚本来尝试不同的配置组合，不会重复安装的，请放心。
 - 不同的配置组合会影响速度，可以自己多折腾折腾。
 - 请勿盲目与SS或者SSR对比，只要能高速扶墙就是好东西，按个人喜好选择就好了。

## 一键脚本 ##


    wget --no-check-certificate https://raw.githubusercontent.com/Moexin/Easy-V2ray/master/v2ray.sh && bash v2ray.sh

安装完成后下载VPS上 /root/config.json 客户端配置文件，与V2ray放在同一个文件夹下。（V2ray下载地址：https://github.com/v2ray/v2ray-core/releases/latest）然后运行V2ray，设置代理为http代理，代理服务器地址：127.0.0.1，代理端口为1080，你就进入自由的互联网啦！
**系统支持**

 - Debian 7
 - Debian 8 
 - Ubuntu 14 
 - Ubuntu 16 
 - CentOS 7 

## 注意事项 ##

 - 不支持CentOS6系统 
 - 如需在手机上使用Shadowrocket软件连接Vmess协议，请勿在脚本内开启mKCP协议和HTTP头部伪装功能
 - 客户端默认是http代理，直接在IE里设置为127.0.0.1:1080即可
 - 如需启用socks，请在客户端文件config.json中把 http 改为 socks 重启系统须自己手动把防火墙关闭
 - 请使用Xshell连接以支持中文的正常显示

**缺点**

此脚本会关闭防火墙，仅适用于纯粹用于扶墙的VPS，请勿在生产环境下使用
## 感谢 ##
雨落无声
V2ray



  [1]: https://www.v2ray.com/
  [2]: https://github.com/Moexin/Easy-V2ray