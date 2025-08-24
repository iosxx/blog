---
title: "obsidian手机搭建hugo"
date: "2025-08-24T04:38:46+0800"
tags:
  - 鼓捣
feature: "https://images.unsplash.com/photo-1703085467946-8fba54ce6dd9?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3wzNjAwOTd8MHwxfHNlYXJjaHwxfHwlRTYlOTUlOTklRTclQTglOEJ8ZW58MHwwfHx8MTc1NjAxNzA2Mnww&ixlib=rb-4.1.0&q=80&w=1080"
published: true
hideInList: false
isTop: false
---

这应该是就目前为止最全面的obsidian搭建博客的教程了，全程手机操作
<!--more-->


![](images/79cdd80adcfa291bd063f1fa9b0c7926.webp)


先说好，我是邪修
正道人士退避

# 第一步
先去github找一个你喜欢博客源码，
搜索blog，hugo，hexo这些。
文明人做的事怎么是偷呢，理论上只要把代码上传github都属于开源行为
只要不用做商用，然后注明来源基本上就可以使用。

我用的是木木木木木大佬的源码
[关于 :: 木木木木木](https://immmmm.com/about/)

然后还有两个也挺好，这两个大佬也是把源码贴了出来

这都是我天天混木木大佬评论区认识的人脉，虽然人家不认识我，嘿嘿

也贴出来给你们选择吧
[我 - 空白Koobai](https://koobai.com/about/) 空白大佬好像没有申明他的源码在哪里，但是我在github有看到过他

[蜗牛](https://www.eallion.com/about/)
蜗牛大佬的也挺好

用这些大佬已经改好的大佬的源码其实好处还是挺多的，我们可以在他们的基础上折腾，然后这些明确给源码地址的大佬，他们的文章好多都有写怎么折腾出来的这些功能

fork，然后你自己想办法git下来，一定要git下来，而不是下载下来
推荐软件 termux
需要下载到外部文件夹，方便obsidian打开
`pkg install termux-api
termux-setup-storage`

# 第二步

用obsidian打开这个文件

打开设置-文件与链接，按照下图设置
![](/images/Screenshot_20250824_122957_md_obsidian_MainActivity_edit_1471869296502744.webp)

模板的话给根据源码文章自己设置

然后推荐下我目前用的插件，每一个都很有用
![](/images/Screenshot_20250824_123401_md_obsidian_MainActivity_edit_1472118788450721.webp)

1.粘贴链接自动获取描述（我刚加的）
2.上传文件的
3.转换图片为webp
4.个人喜好，搜索图片并自动添加的
5.这是个调整格式的，我都没用，主要用了里面自动替换功能（如图片格式）
如：前面添加github cdn格式
[jsdelivr](https://cdn.jsdelivr.net/)
当然我用在调整本地图片格式上，相信我你会用到，我搜过，没有人写过这个功能，但是确实解决了我的大问题

# 第三步
把源码中必要的部分修改一下
尤其是评论的链接，别自己的评论跑到大佬的邮箱里别去打扰到人家
林木木大佬twikoo评论修改地址，
直接搜envId
大致修改就可以把文件通过git插件上传到github
然后发布即可
林木木木木木大佬这个主要是发布到cloudflare ，选择hugo程序发布，添加变量HUGO_VERSION ＝ 0.92.0
[使用 Obsidian 一键发布博客 \| 蓝色大树🌲 — Yao's Blog](https://yaofun.top/posts/2024/03/%E4%BD%BF%E7%94%A8-obsidian-%E4%B8%80%E9%94%AE%E5%8F%91%E5%B8%83%E5%8D%9A%E5%AE%A2/)这个大佬提供的教程，他也开源了，也可以选择


然后蜗牛大佬的发布方式主要是用github action，想要多元化的方式建议用这个貌似有edgeone，cloudflare，还有github pages，喜欢其他的也可以自己加

vercel也可以直接套，但是我不太推荐，他的部署次数貌似有些少，反正很坑的感觉，喜欢的也可以试试

# 最后一步

基本上到这里了你就可以自由自在的用手机发布博客了。