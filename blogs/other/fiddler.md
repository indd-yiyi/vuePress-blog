---
title: Fiddler是一款免费网络代理调试工具
date: 2020-12-20
cover: https://pan.zealsay.com/mweb/blog/WechatIMG5.png
tags:
 - fiddler
categories:
 -  技术笔记
---
<br />Fiddler是一款免费网络代理调试工具。<br /> <br />Fiddler是一个蛮好用的抓包工具，可以将网络传输发送与接受的数据包进行截获、重发、编辑、转存等操作。也可以用来检测网络安全。反正好处多多，举之不尽呀！<br /> <br />当年学习的时候也蛮费劲，一些蛮实用隐藏的小功能用了之后就忘记了，每次去网站上找也很麻烦，所以搜集各大网络的资料，总结了一些常用的功能。<br />
<br />

<a name="QuE0P"></a>
## 一、Fiddler 下载

<br />注意：Fiddler2需要.NET v2，Fiddler4需要.NET v4，不过这些也不用怎么管，下载用默认的就好了。

官网下载：[https://www.telerik.com/fiddler](https://www.telerik.com/fiddler)<br />百度网盘链接: [https://pan.baidu.com/s/14C0bOTICZADj03ZGx_eygw](https://pan.baidu.com/s/14C0bOTICZADj03ZGx_eygw) 提取码: chdi<br />
<br />

<a name="c8OSn"></a>
## 二、Fiddler 安装

<br />由于是Fiddler只支持Windows XP到Windows 10，安装我就不多说了，exe傻瓜式安装，大家都能明白。

<a name="z33T6"></a>
## 三、Fiddler 使用

<br />先给大家简单说一下，Fiddler这款抓包工具，与别人工具还是有所不同的。<br />Fiddler是通过改写HTTP代理，让数据从它那通过，来监控并且截取到数据。当然Fiddler很屌，在打开它的那一瞬间，它就已经设置好了浏览器的代理了。当你关闭的时候，它又帮你把代理还原了，是不是很方便？<br />

<a name="oDUNE"></a>
#### 1、开启或关闭抓包功能
Fiddler想要抓到数据包，要确保Capture Traffic是开启，在“File –> Capture Traffic”。开启后再左下角会有显示，当然也可以直接点击左下角的图标来关闭/开启抓包功能。<br />
<br />![100-1.png](https://cdn.nlark.com/yuque/0/2021/png/2899468/1617861476716-251d6362-0d32-401e-82c7-78b0a20a5b2f.png#align=left&display=inline&height=634&margin=%5Bobject%20Object%5D&name=100-1.png&originHeight=845&originWidth=895&size=102533&status=done&style=none&width=671)<br />
<br />

<a name="DJYIA"></a>
#### 2、字段说明
Fiddler开始工作了，抓到的数据包就会显示在列表里面，下面总结了这些都是什么意思？<br />
<br />![200-1.png](https://cdn.nlark.com/yuque/0/2021/png/2899468/1617861464821-50ab9d1f-9df7-49bd-9f2e-19877aab12c7.png#align=left&display=inline&height=425&margin=%5Bobject%20Object%5D&name=200-1.png&originHeight=567&originWidth=867&size=79269&status=done&style=none&width=650)<br />
<br />


| **名称** | **含义** |
| :--- | :--- |
| # | 抓取HTTP Request的顺序，从1开始，以此递增 |
| Result | HTTP状态码 |
| Protocol | 请求使用的协议，如HTTP/HTTPS/FTP等 |
| Host | 请求地址的主机名 |
| URL | 请求资源的位置 |
| Body | 该请求的大小 |
| Caching | 请求的缓存过期时间或者缓存控制值 |
| Content-Type | 请求响应的类型 |
| Process | 发送此请求的进程：进程ID |
| Comments | 允许用户为此回话添加备注 |
| Custom | 允许用户设置自定义值 |
| **图标** | **含义** |
| [![](https://cdn.nlark.com/yuque/0/2021/gif/2899468/1617861512369-7709acdc-a3e7-4d13-acea-c92034622f1e.gif#align=left&display=inline&height=17&margin=%5Bobject%20Object%5D&originHeight=17&originWidth=13&size=0&status=done&style=none&width=13)](https://www.fujieace.com/wp-content/uploads/2019/08/1.gif?x73259) | 请求已经发往服务器 |
| [![](https://cdn.nlark.com/yuque/0/2021/gif/2899468/1617861512376-bb3ead73-3c3b-4d0f-9218-ec71819cdceb.gif#align=left&display=inline&height=17&margin=%5Bobject%20Object%5D&originHeight=17&originWidth=13&size=0&status=done&style=none&width=13)](https://www.fujieace.com/wp-content/uploads/2019/08/2.gif?x73259) | 已从服务器下载响应结果 |
| [![](https://cdn.nlark.com/yuque/0/2021/gif/2899468/1617861512333-ea15da21-5683-40c5-9ae4-79b75aae458f.gif#align=left&display=inline&height=17&margin=%5Bobject%20Object%5D&originHeight=17&originWidth=15&size=0&status=done&style=none&width=15)](https://www.fujieace.com/wp-content/uploads/2019/08/3.gif?x73259) | 请求从断点处暂停 |
| [![](https://cdn.nlark.com/yuque/0/2021/gif/2899468/1617861512428-7721a535-aa48-4689-9cab-263295e08f88.gif#align=left&display=inline&height=17&margin=%5Bobject%20Object%5D&originHeight=17&originWidth=15&size=0&status=done&style=none&width=15)](https://www.fujieace.com/wp-content/uploads/2019/08/4.gif?x73259) | 响应从断点处暂停 |
| [![](https://cdn.nlark.com/yuque/0/2021/gif/2899468/1617861512513-2a2357ce-8be7-4dfa-b8c9-072df3e2f1ca.gif#align=left&display=inline&height=16&margin=%5Bobject%20Object%5D&originHeight=16&originWidth=16&size=0&status=done&style=none&width=16)](https://www.fujieace.com/wp-content/uploads/2019/08/5.gif?x73259) | 请求使用 HTTP 的 HEAD 方法，即响应没有内容（Body） |
| [![](https://cdn.nlark.com/yuque/0/2021/png/2899468/1617861512431-81967cd2-511d-4772-a425-d29bdd2e10c1.png#align=left&display=inline&height=17&margin=%5Bobject%20Object%5D&originHeight=17&originWidth=16&size=0&status=done&style=none&width=16)](https://www.fujieace.com/wp-content/uploads/2019/08/6.png?x73259) | 请求使用 HTTP 的 POST 方法 |
| [![](https://cdn.nlark.com/yuque/0/2021/gif/2899468/1617861512569-e8b37e4f-d973-4f8c-8a0e-47e0e7eef9b3.gif#align=left&display=inline&height=15&margin=%5Bobject%20Object%5D&originHeight=15&originWidth=14&size=0&status=done&style=none&width=14)](https://www.fujieace.com/wp-content/uploads/2019/08/7.gif?x73259) | 请求使用 HTTP 的 CONNECT 方法，使用 HTTPS 协议建立连接隧道 |
| [![](https://cdn.nlark.com/yuque/0/2021/gif/2899468/1617861512660-76ea9bab-a212-431e-8e70-2e455c254728.gif#align=left&display=inline&height=17&margin=%5Bobject%20Object%5D&originHeight=17&originWidth=15&size=0&status=done&style=none&width=15)](https://www.fujieace.com/wp-content/uploads/2019/08/8.gif?x73259) | 响应是 HTML 格式 |
| [![](https://cdn.nlark.com/yuque/0/2021/gif/2899468/1617861512649-e8d39d47-dd9d-47f5-a6e3-16d32a6d2bf8.gif#align=left&display=inline&height=16&margin=%5Bobject%20Object%5D&originHeight=16&originWidth=16&size=0&status=done&style=none&width=16)](https://www.fujieace.com/wp-content/uploads/2019/08/9.gif?x73259) | 响应是一张图片 |
| [![](https://cdn.nlark.com/yuque/0/2021/gif/2899468/1617861512685-897d9016-dc7a-4cfb-b275-3c02d137a214.gif#align=left&display=inline&height=17&margin=%5Bobject%20Object%5D&originHeight=17&originWidth=17&size=0&status=done&style=none&width=17)](https://www.fujieace.com/wp-content/uploads/2019/08/10.gif?x73259) | 响应是脚本格式 |
| [![](https://cdn.nlark.com/yuque/0/2021/gif/2899468/1617861512786-363b228f-1aa2-4c92-a1db-86287c278c14.gif#align=left&display=inline&height=17&margin=%5Bobject%20Object%5D&originHeight=17&originWidth=16&size=0&status=done&style=none&width=16)](https://www.fujieace.com/wp-content/uploads/2019/08/11.gif?x73259) | 响应是 CSS 格式 |
| [![](https://cdn.nlark.com/yuque/0/2021/gif/2899468/1617861512810-e01674c4-478c-41b8-9533-a1f66159bf1d.gif#align=left&display=inline&height=17&margin=%5Bobject%20Object%5D&originHeight=17&originWidth=17&size=0&status=done&style=none&width=17)](https://www.fujieace.com/wp-content/uploads/2019/08/12.gif?x73259) | 响应是 XML 格式 |
| [![](https://cdn.nlark.com/yuque/0/2021/png/2899468/1617861513829-162bf4d9-c2f5-4046-941f-19a2f71da96f.png#align=left&display=inline&height=17&margin=%5Bobject%20Object%5D&originHeight=17&originWidth=16&size=0&status=done&style=none&width=16)](https://www.fujieace.com/wp-content/uploads/2019/08/13.png?x73259) | 响应是 JSON 格式 |
| [![](https://cdn.nlark.com/yuque/0/2021/png/2899468/1617861512905-c7fc8271-d6d6-4c04-8dbc-2f16cdabb03c.png#align=left&display=inline&height=16&margin=%5Bobject%20Object%5D&originHeight=16&originWidth=14&size=0&status=done&style=none&width=14)](https://www.fujieace.com/wp-content/uploads/2019/08/14.png?x73259) | 响应是一个音频文件 |
| [![](https://cdn.nlark.com/yuque/0/2021/png/2899468/1617861513562-ab06a594-5df8-4a20-b961-cd89b600cd90.png#align=left&display=inline&height=16&margin=%5Bobject%20Object%5D&originHeight=16&originWidth=15&size=0&status=done&style=none&width=15)](https://www.fujieace.com/wp-content/uploads/2019/08/15.png?x73259) | 响应是一个视频文件 |
| [![](https://cdn.nlark.com/yuque/0/2021/png/2899468/1617861512973-d43c3aad-9e87-42a5-a1a2-0030efe0d283.png#align=left&display=inline&height=15&margin=%5Bobject%20Object%5D&originHeight=15&originWidth=16&size=0&status=done&style=none&width=16)](https://www.fujieace.com/wp-content/uploads/2019/08/16.png?x73259) | 响应是一个 SilverLight |
| [![](https://cdn.nlark.com/yuque/0/2021/png/2899468/1617861513126-ff3d781b-77cf-498a-ae65-dfeeeab3c502.png#align=left&display=inline&height=16&margin=%5Bobject%20Object%5D&originHeight=16&originWidth=13&size=0&status=done&style=none&width=13)](https://www.fujieace.com/wp-content/uploads/2019/08/17.png?x73259) | 响应是一个 FLASH |
| [![](https://cdn.nlark.com/yuque/0/2021/png/2899468/1617861513195-99d5b744-fc45-42c3-a6f7-d5e5d317fa7d.png#align=left&display=inline&height=16&margin=%5Bobject%20Object%5D&originHeight=16&originWidth=14&size=0&status=done&style=none&width=14)](https://www.fujieace.com/wp-content/uploads/2019/08/18.png?x73259) | 响应是一个字体 |
| [![](https://cdn.nlark.com/yuque/0/2021/gif/2899468/1617861513214-698d2330-da54-41a2-bc8e-88f6d27b566e.gif#align=left&display=inline&height=15&margin=%5Bobject%20Object%5D&originHeight=15&originWidth=13&size=0&status=done&style=none&width=13)](https://www.fujieace.com/wp-content/uploads/2019/08/19.gif?x73259) | 普通响应成功 |
| [![](https://cdn.nlark.com/yuque/0/2021/gif/2899468/1617861513394-1d743cbd-e328-4dde-81f7-94de51a700af.gif#align=left&display=inline&height=14&margin=%5Bobject%20Object%5D&originHeight=14&originWidth=14&size=0&status=done&style=none&width=14)](https://www.fujieace.com/wp-content/uploads/2019/08/20.gif?x73259) | 响应是 HTTP/300、301、302、303 或 307 重定向 |
| [![](https://cdn.nlark.com/yuque/0/2021/gif/2899468/1617861513429-88163944-abb3-4fcc-a54b-020f0bd1fdc3.gif#align=left&display=inline&height=16&margin=%5Bobject%20Object%5D&originHeight=16&originWidth=17&size=0&status=done&style=none&width=17)](https://www.fujieace.com/wp-content/uploads/2019/08/21.gif?x73259) | 响应是 HTTP/304（无变更）：使用缓存文件 |
| [![](https://cdn.nlark.com/yuque/0/2021/gif/2899468/1617861513452-f5312f0b-5d24-4cbf-983b-abf5702284df.gif#align=left&display=inline&height=18&margin=%5Bobject%20Object%5D&originHeight=18&originWidth=12&size=0&status=done&style=none&width=12)](https://www.fujieace.com/wp-content/uploads/2019/08/22.gif?x73259) | 响应需要客户端证书验证 |
| [![](https://cdn.nlark.com/yuque/0/2021/gif/2899468/1617861513488-26944858-6484-4533-a992-e1c15ba6c3dd.gif#align=left&display=inline&height=14&margin=%5Bobject%20Object%5D&originHeight=14&originWidth=14&size=0&status=done&style=none&width=14)](https://www.fujieace.com/wp-content/uploads/2019/08/23.gif?x73259) | 服务端错误 |
| [![](https://cdn.nlark.com/yuque/0/2021/gif/2899468/1617861513671-c6d75ff5-9169-4f79-867c-423fe120e359.gif#align=left&display=inline&height=17&margin=%5Bobject%20Object%5D&originHeight=17&originWidth=16&size=0&status=done&style=none&width=16)](https://www.fujieace.com/wp-content/uploads/2019/08/24.gif?x73259) | 会话被客户端、Fiddler 或者服务端终止 |



<a name="1gfUh"></a>
#### 3、Statistics 请求的性能数据分析
**<br />
<br />好了，左边看完了，现在可以看右边了；随意点击一个请求，就可以看到Statistics关于HTTP请求的性能以及数据分析了。

<a name="tjPOV"></a>
#### 4、Inspectors 查看数据内容
**<br />
<br />Inspectors是用于查看会话的内容，上半部分是请求的内容，下半部分是响应的内容；<br />
<br />![400-1.png](https://cdn.nlark.com/yuque/0/2021/png/2899468/1617862389682-94f7911d-853d-483b-b5f8-d415cbf9cb9e.png#align=left&display=inline&height=547&margin=%5Bobject%20Object%5D&name=400-1.png&originHeight=547&originWidth=757&size=36796&status=done&style=none&width=757)<br />

<a name="sAPmh"></a>
#### 5、AutoResponder 允许拦截指定规则的请求
**<br />AutoResponder允许你拦截指定规则的求情，并返回本地资源或Fiddler资源，从而代替服务器响应。<br />
<br />
<br />看下图5步，我将“baidu”这个关键字与我电脑“f:\Users\YukiO\Pictures\boy.jpeg”这张图片绑定了，点击“Save”保存后勾选“Enable rules”，再访问baidu，就会被劫持。<br />
<br />
<br />![](https://cdn.nlark.com/yuque/0/2021/png/2899468/1617872324807-100f5ba0-2be2-49b8-b481-c9e5948f2802.png#align=left&display=inline&height=508&margin=%5Bobject%20Object%5D&originHeight=617&originWidth=896&size=0&status=done&style=none&width=737)<br />
<br />![image.png](https://cdn.nlark.com/yuque/0/2021/png/2899468/1618298538158-0884eb0f-74b9-4ec5-947e-644b801c2f69.png#align=left&display=inline&height=357&margin=%5Bobject%20Object%5D&name=image.png&originHeight=357&originWidth=1239&size=205502&status=done&style=none&width=1239)<br />这个玩意有很多匹配规则，如：<br />
<br />

1. 字符串匹配（默认）：只要包含指定字符串（不区分大小写），全部认为是匹配


<br />字符串匹配（baidu） 是否匹配<br />
<br />

> [http://www.baidu.com](http://www.baidu.com) 匹配
> [http://pan.baidu.com](http://pan.baidu.com) 匹配
> [http://tieba.baidu.com](http://tieba.baidu.com) 匹配


<br />

2. 正则表达式匹配：以“regex:”开头，使用正则表达式来匹配，这个是区分大小写的


<br />字符串匹配（regex:.+.(jpg | gif | bmp ) $） 是否匹配<br />
<br />

> [http://bbs.fishc.com/Path1/query=foo.bmp&bar](http://bbs.fishc.com/Path1/query=foo.bmp&bar) 不匹配
> [http://bbs.fishc.com/Path1/query=example.gif](http://bbs.fishc.com/Path1/query=example.gif) 匹配
> [http://bbs.fishc.com/Path1/query=example.bmp](http://bbs.fishc.com/Path1/query=example.bmp) 匹配
> [http://bbs.fishc.com/Path1/query=example.Gif](http://bbs.fishc.com/Path1/query=example.Gif) 不匹配


<br />
<br />

<a name="VjT1T"></a>
#### 6、Composer 自定义请求发送服务器
**<br />Composer允许自定义请求发送到服务器，可以手动创建一个新的请求，也可以在会话表中，拖拽一个现有的请求<br />
<br />Parsed模式下你只需要提供简单的URLS地址即可（如下图，也可以在RequestBody定制一些属性，如模拟浏览器User-Agent）

![600-1.png](https://cdn.nlark.com/yuque/0/2021/png/2899468/1618300511998-dc5ed805-51f2-4d80-81e2-cb7027e77d63.png#align=left&display=inline&height=625&margin=%5Bobject%20Object%5D&name=600-1.png&originHeight=833&originWidth=894&size=45374&status=done&style=none&width=671)<br />

<a name="ckX2j"></a>
#### 7、Filters 请求过滤规则
Fiters 是过滤请求用的，左边的窗口不断的更新，当你想看你系统的请求的时候，你刷新一下浏览器，一大片不知道哪来请求，看着碍眼，它还一直刷新你的屏幕。这个时候通过过滤规则来过滤掉那些不想看到的请求。<br /> <br />勾选左上角的Use Filters开启过滤器，这里有两个最常用的过滤条件：Zone和Host<br />
<br />
<br />
<br />
<br />![700-1.png](https://cdn.nlark.com/yuque/0/2021/png/2899468/1618378319247-5dccba1b-e2e9-4c92-b121-ec80c5190c4f.png#align=left&display=inline&height=563&margin=%5Bobject%20Object%5D&name=700-1.png&originHeight=563&originWidth=758&size=27181&status=done&style=none&width=758)<br />Zone 指定只显示内网（Intranet）或互联网（Internet）的内容：<br />
<br />
<br />![701.png](https://cdn.nlark.com/yuque/0/2021/png/2899468/1618378345277-8cf0b38e-7d7a-47bc-9a46-d8a65c543844.png#align=left&display=inline&height=175&margin=%5Bobject%20Object%5D&name=701.png&originHeight=175&originWidth=626&size=5299&status=done&style=none&width=626)<br />
<br />Host 指定显示某个域名下的会话：![702.png](https://cdn.nlark.com/yuque/0/2021/png/2899468/1618378374772-3668295b-665f-438b-a36b-18e0e946eb7c.png#align=left&display=inline&height=180&margin=%5Bobject%20Object%5D&name=702.png&originHeight=180&originWidth=627&size=6874&status=done&style=none&width=627)<br />如果框框为黄色（如图），表示修改未生效，点击红圈里的文字即可!

<a name="wgkPk"></a>
#### 8、Timeline 请求响应时间![800-1.png](https://cdn.nlark.com/yuque/0/2021/png/2899468/1618378412410-40d22c8e-27c2-4e1e-b7b7-0ad4ddd537b9.png#align=left&display=inline&height=199&margin=%5Bobject%20Object%5D&name=800-1.png&originHeight=199&originWidth=726&size=8359&status=done&style=none&width=726)
<a name="4txbr"></a>
#### 9、Fiddler 设置解密HTTPS的网络数据
**<br />Fiddler可以通过伪造CA证书来欺骗浏览器和服务器。Fiddler是个很会装逼的好东西，大概原理就是在浏览器面前Fiddler伪装成一个HTTPS服务器，而在真正的HTTPS服务器面前Fiddler又装成浏览器，从而实现解密HTTPS数据包的目的。

解密HTTPS需要手动开启，依次点击：

（1）、Tools –> Fiddler Options –> HTTPS；![900-1.png](https://cdn.nlark.com/yuque/0/2021/png/2899468/1618378514660-ccc89c73-5343-483a-95f6-c8d3841cf0ac.png#align=left&display=inline&height=514&margin=%5Bobject%20Object%5D&name=900-1.png&originHeight=514&originWidth=896&size=54805&status=done&style=none&width=896)

（2）、勾选Decrypt HTTPS Traffic

![901.png](https://cdn.nlark.com/yuque/0/2021/png/2899468/1618378535024-635b3ea8-3bbb-47d8-8432-d6824c5addb4.png#align=left&display=inline&height=628&margin=%5Bobject%20Object%5D&name=901.png&originHeight=628&originWidth=888&size=80831&status=done&style=none&width=888)<br />（3）、点击OK![902.png](https://cdn.nlark.com/yuque/0/2021/png/2899468/1618378554996-66336eea-2733-4b7b-84c9-7866cd980923.png#align=left&display=inline&height=625&margin=%5Bobject%20Object%5D&name=902.png&originHeight=625&originWidth=893&size=71541&status=done&style=none&width=893)

<a name="aBoOD"></a>
#### 10、Fiddler 内置命令与断点
Fiddler还有一个藏的很深的命令框，就是眼前，我用了几年的Fiddler都没有发现它，偶尔在别人的文章发现还有这个小功能，还蛮好用的，整理下记录在这里。![1000-1.png](https://cdn.nlark.com/yuque/0/2021/png/2899468/1618378596931-75b513a2-6e0a-4645-b1cc-0c3bd42dc603.png#align=left&display=inline&height=399&margin=%5Bobject%20Object%5D&name=1000-1.png&originHeight=399&originWidth=675&size=58351&status=done&style=none&width=675)<br />
<br />FIddler断点功能就是将请求截获下来，但是不发送，这个时候你可以干很多事情，比如说，把包改了，再发送给服务器君。还有balabala一大堆的事情可以做，就不举例子了。

| **命令** | **对应请求项** | **介绍** | **示例** |
| :--- | :--- | :--- | :--- |
| ? | All | 问号后边跟一个字符串，可以匹配出包含这个字符串的请求 | ?google |
| > | Body | 大于号后面跟一个数字，可以匹配出请求大小，大于这个数字请求 | >1000 |
| < | Body | 小于号跟大于号相反，匹配出请求大小，小于这个数字的请求 | <100 |
| = | Result | 等于号后面跟数字，可以匹配HTTP返回码 | =200 |
| @ | Host | @后面跟Host，可以匹配域名 | @www.baidu.com |
| select | Content-Type | select后面跟响应类型，可以匹配到相关的类型 | select image |
| cls | All | 清空当前所有请求 | cls |
| dump | All | 将所有请求打包成saz压缩包，保存到“我的文档\\Fiddler2\\Captures”目录下 | dump |
| start | All | 开始监听请求 | start |
| stop | All | 停止监听请求 | stop |
| **断点命令** |  |  |  |
| bpafter | All | bpafter后边跟一个字符串，表示中断所有包含该字符串的请求 | bpafter baidu（输入bpafter解除断点） |
| bpu | All | 跟bpafter差不多，只不过这个是收到请求了，中断响应 | bpu baidu（输入bpu解除断点） |
| bps | Result | 后面跟状态吗，表示中断所有是这个状态码的请求 | bps 200（输入bps解除断点） |
| bpv / bpm | HTTP方法 | 只中断HTTP方法的命令，HTTP方法如POST、GET | bpv get（输入bpv解除断点） |
| g / go | All | 放行所有中断下来的请求 | g |


<br />bpafter 命令示例：<br />![2000.png](https://cdn.nlark.com/yuque/0/2021/png/2899468/1618378658215-09a83ce6-a25c-4b65-bafa-4f34c0f70d4c.png#align=left&display=inline&height=408&margin=%5Bobject%20Object%5D&name=2000.png&originHeight=408&originWidth=718&size=37404&status=done&style=none&width=718)![20001.png](https://cdn.nlark.com/yuque/0/2021/png/2899468/1618378665346-79677d4f-ad82-4922-9251-4771ac4b1829.png#align=left&display=inline&height=408&margin=%5Bobject%20Object%5D&name=20001.png&originHeight=408&originWidth=718&size=34622&status=done&style=none&width=718)

断点命令：<br />断点可以直接点击Fiddler下图的图标位置，就可以设置全部请求的断点，断点的命令可以精确设置需要截获那些请求。如下示例：![3000.png](https://cdn.nlark.com/yuque/0/2021/png/2899468/1618378698199-71aa8708-0289-4dab-8531-d8b99174338f.png#align=left&display=inline&height=655&margin=%5Bobject%20Object%5D&name=3000.png&originHeight=655&originWidth=987&size=78821&status=done&style=none&width=987)
