---
layout: post
title:  "魔改版BBR一键安装脚本 For Debian8 Ubuntu16 +"
date:   2017-07-31 13:46:40
categories: Skill
---
## 简介 ##
BBR相信大家都不陌生，是谷歌开发的一个存在于Linux内核中的拥塞算法。为了优化国内与服务器之间的网络质量，loc的大佬专门魔改改进了下这个BBR，成为了新的BBR魔改版。我也就乘机水一篇文章好了~在Debian 8 和Ubuntu16 + 系统上一键部署魔改版BBR，自动换内核成 4.10.15 ，自动安装Headers。用户只需要将系统安装成 Debian 8 或者 Ubuntu 16 即可，剩下的交给脚本来吧。
Github地址:[https://github.com/FunctionClub/YankeeBBR][1]
![请输入图片描述][2]

## 参考资料 ##
魔改BBR原帖：[http://www.hostloc.com/thread-372277-1-2.html][3]
萌新教程: [http://www.hostloc.com/thread-372335-1-1.html][4]
脚本技术： [https://doub.io/wlzy-16/][5]
**部分商家的VPS可能会遇到换内核之后无法启动系统的情况，所以请运行脚本前一定要备份好重要数据！！**
## 安装使用 ##

    wget -N --no-check-certificate https://raw.githubusercontent.com/FunctionClub/YankeeBBR/master/bbr.sh && bash bbr.sh install

安装过程中如果出现这张图片，请选择NO 来删除其他内核：
![请输入图片描述][6]
然后根据提示重启系统。
重启完成后，运行

    bash bbr.sh start

即可启动魔改版BBR。
## 查看魔改BBR状态 ##

    sysctl net.ipv4.tcp_available_congestion_control

如果看到有 tsunami 就表示开启成功！
![请输入图片描述][7]

> 本文删减改自：
> [https://ylws.me/tech/68.html][8]


  [1]: https://github.com/FunctionClub/YankeeBBR
  [2]: http://imglf0.nosdn.127.net/img/cEczVHlUNlVvWHljdlZ5YlJBU1o0QTB3SUxIZzhVL3h6WE1HRmxJdk53bGI1Ui82S0tOczBBPT0.png?imageView&thumbnail=1680x0&quality=96&stripmeta=0&type=jpg%7Cwatermark&type=2&text=wqkgbG1lb28uY29tIC8gaW1nLWxtZW9vLmxvZnRlci5jb20=&font=bXN5aA==&gravity=southwest&dissolve=30&fontsize=340&dx=16&dy=20&stripmeta=0
  [3]: http://www.hostloc.com/thread-372277-1-2.html
  [4]: http://www.hostloc.com/thread-372335-1-1.html
  [5]: https://doub.io/wlzy-16/
  [6]: http://imglf.nosdn.127.net/img/cEczVHlUNlVvWHljdlZ5YlJBU1o0SDdkWFNrNW8vQlpFU3hiTi9DWXdFMVl1OTVNSVB6empnPT0.png?imageView&thumbnail=1680x0&quality=96&stripmeta=0&type=jpg%7Cwatermark&type=2&text=wqkgbG1lb28uY29tIC8gaW1nLWxtZW9vLmxvZnRlci5jb20=&font=bXN5aA==&gravity=southwest&dissolve=30&fontsize=340&dx=16&dy=20&stripmeta=0
  [7]: http://imglf1.nosdn.127.net/img/cEczVHlUNlVvWHljdlZ5YlJBU1o0QkpyL1B0L29rdU9rWHNRRzBGWjhGOWNnT094R3paVlJnPT0.png?imageView&thumbnail=1680x0&quality=96&stripmeta=0&type=jpg%7Cwatermark&type=2&text=wqkgbG1lb28uY29tIC8gaW1nLWxtZW9vLmxvZnRlci5jb20=&font=bXN5aA==&gravity=southwest&dissolve=30&fontsize=340&dx=16&dy=20&stripmeta=0
  [8]: https://ylws.me/tech/68.html