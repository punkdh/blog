---
layout: post
title: 打造自己专属的chrome终极形态
date: 2019-1-13
tag: GEEK
---

# 背景

因为找到了好设备可以登录谷歌账户了，可以在N台电脑上同步自己的各种浏览器设定和插件，就果断抛弃了360极速这个国产替代品，感谢多年的陪伴。
写个文章记录一下这周对chrome的学习和摸索成果

# 装备1- 密码保存

之前360的极速的密码总会有各种奇怪的事情发生已经莫名其妙丢过几次了，而且在另一台电脑上同步也容易出现问题，safari 的密码保存是很美妙的，我真的是很烦输入账户和密码的人， safari可以保存淘宝账户、微博账户，但360极速不行，chrome本来也不能存微博啥的，装了一个 autocomplete On!插件可以强制网页启动自动填充这些不允许自动填充的破网站了。

![autocomplete On!](https://upload-images.jianshu.io/upload_images/10043074-ed1a0e4bc818caa4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
密码工具可以帮助在注册软件的时候可以建议自动填充一些乱序密码，提高安全性。

![chrome密码工具](https://upload-images.jianshu.io/upload_images/10043074-ebe14e2dba990bce.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# 装备2- 浏览器插件应用

![网上应用商店](https://upload-images.jianshu.io/upload_images/10043074-c5a19ad3bd7a05a4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
用电脑的大部分时间还是在浏览器上的，随着网速越来越快所有应用都会渐渐转向B/S 架构，所有基本没啥是不能在浏览器上完成的，包括PS，AI，CAD，3Dmax，包括写代码等这些事都是可以在浏览器网页上完成的。

有需求的可以参考下面这个网站：
- https://uzer.me/z/apps
![WEB软件窗口](https://upload-images.jianshu.io/upload_images/10043074-2d8f2416906933fb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 我的应用插件清单

- Evernote Web Clipper：把有用的网页剪藏到印象笔记
- Adblock Plus：各种广告拦截
- Autocomplete On!：强制可以自动填充密码
- Fatkun图片批量下载：找出当前页面的所有图片，提供按分辨率、链接等筛选图片
- OneTab：节省高达95％的内存，并减轻标签页混乱现象
- Rememberry - 翻译和记住：划词翻译
- Save Image As PNG：把webpic 格式转为png下载
- View Image：以图搜图
- 京价保 - 京东价保助手：自动抢京东里的各种券
- 流量节省程序：用了半个月似乎1M流量都没节省（- -）
- 猫抓：自动抓取视频网站的视频地址可以提供下载（下片神器）
- 眼不见心不烦（新浪微博）：以无限制地屏蔽关键词、用户、来源，去除页面广告和推广微博，反刷屏

# 装备3- tampermonkey（猴油插件）

这个需要单独拿出来说，猴油说白了个就一个帮助你在网页运行自定义脚本的的插件，包罗万象

![猴油插件](https://upload-images.jianshu.io/upload_images/10043074-d129543c85a7887b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- AC-baidu:重定向优化百度搜狗谷歌搜索

不好解释作用，看图

![搜索结果优化](https://upload-images.jianshu.io/upload_images/10043074-8b4ebd7e55454fc7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![搜索结果优化2](https://upload-images.jianshu.io/upload_images/10043074-5abc493e9f302406.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 全网音乐一键免费下载

![音乐下载](https://upload-images.jianshu.io/upload_images/10043074-49ec8906a00dce55.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 购物党自动比价工具

![自动比价及历史曲线](https://upload-images.jianshu.io/upload_images/10043074-e986450616ba251a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- Yet Another Weibo Filter：看真正想看的微博

![微博过滤器](https://upload-images.jianshu.io/upload_images/10043074-5fa17d7857e39353.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 豆瓣资源下载大师：1秒搞定豆瓣电影|音乐|图书下载

> 点到左边的资源网站就能直接下载

![豆瓣资源下载大师](https://upload-images.jianshu.io/upload_images/10043074-9b12937309555d95.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 百度网盘直接下载助手：禁止弹出百度网盘下载
- 知乎免登录：不用登陆就可以看知乎答案
- 破解VIP会员视频集合：一键破解[优酷|腾讯|乐视|爱奇艺|芒果|AB站|音悦台]
- 网页限制解除：禁止复制啥的网站都直接解禁，省了我之前想拔文章的时候还需要手动禁用JS，弄完再开启
- MoreMovieRatings ：豆瓣显示IMDB评分
- Endless Google：谷歌搜索结果不用手动翻页
- CNKI 中国知网 PDF 全文下载（特制版）
- 91解析：次数是无限的，但精力是有限的。懂得自然懂。

以上的脚本均能在[Greasy Fork](https://greasyfork.org/zh-CN)搜索到，支持中文。

![猴油脚本网站](https://upload-images.jianshu.io/upload_images/10043074-c985162931fabf39.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
