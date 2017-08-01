---
layout: post
title:  "ViewImage.js - 响应式极简灯箱插件"
date:   2017-04-21 13:46:40
categories: Skill
---
ViewImage.js - 基于jQuery ，Gzip后不足 1kb 的响应式极简灯箱插件

## 获取 ##
你可以直接访问ViewImage的 [GitHub][1] 来获取最新版插件，当然你也可以通过下面的链接下载ViewImage：
[view-image.js][2] or [view-image.min.js][3]
## 引用 ##
首先确保你的页面已经正确引用jQuery（建议2.0+），然后再引用ViewImage.js。

    <script src="//tokinx.github.io/ViewImage/view-image.min.js"></script>

## 启用 ##
我们为您提供了非常简便的初始化方法，方便您对程序进行一些个性化设置并正确启用

    <script>
        jQuery(document).ready(function () {
            jQuery.viewImage({
                'target' : '.view-image img', //需要使用ViewImage的图片
                'exclude': '.exclude img',    //要排除的图片
                'delay'  : 300                //延迟时间
            });
        });
    </script>

## 示例 ##
[https://tokinx.github.io/ViewImage/][4]


  [1]: https://github.com/Tokinx/ViewImage
  [2]: https://tokinx.github.io/ViewImage/view-image.js
  [3]: https://tokinx.github.io/ViewImage/view-image.min.js
  [4]: https://tokinx.github.io/ViewImage/