# 抖音爬虫教程，从0到1，环境配置

<a name="f6SlM"></a>
# 前言
该系列内容主要介绍抖音爬虫的相关过程。因为科研需要，所以选择爬取抖音的视频数据，包括点赞等。爬取思路是首先爬取用户，然后根据用户爬取其对应发布的视频数据。这一个博客我将介绍环境配置。 

---

<a name="2TqZ5"></a>
# 一、抓包软件
<a name="0CaNV"></a>
## 1. 抓包软件选择
这里使用的抓包软件是：[Fiddle](https://www.telerik.com/fiddler)，因为最新版本的Fiddle比较奇怪，所以我还是选择使用老版本的Fiddle(**5.0**版本)。
<a name="8UepP"></a>
## 2. 抓包软件配置
<a name="q3Fqk"></a>
### 2.1. 安装
这里没有什么需要注意的
<a name="Z29qQ"></a>
### 2.2. 配置

- 这是初始界面，选择不更新<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/97322/1607128973296-90423614-3358-400e-81fd-ed7cedd591f1.png#align=left&display=inline&height=698&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1396&originWidth=2850&size=1182354&status=done&style=none&width=1425)
- 这是能用到的两个主要的工具按钮<br />![](https://cdn.nlark.com/yuque/0/2020/png/97322/1607128935664-1b193439-decc-45c3-95b9-4930827fda1b.png#align=left&display=inline&height=155&margin=%5Bobject%20Object%5D&originHeight=155&originWidth=705&size=0&status=done&style=none&width=705)
- 开始配置
> 点击Tools -> Options，就可以看到Options的主面板

![image.png](https://cdn.nlark.com/yuque/0/2020/png/97322/1607129252500-2dfd4de1-58a3-4e30-83dc-d819d8116405.png#align=left&display=inline&height=696&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1392&originWidth=2754&size=1442628&status=done&style=none&width=1377)
> 在Options的主面板中，点击 Https，设置捕获**HTTPS**的包等，详见下图

![image.png](https://cdn.nlark.com/yuque/0/2020/png/97322/1607129011497-5c5fb625-2918-4ad8-aec0-dc2d0d09f36d.png#align=left&display=inline&height=398&margin=%5Bobject%20Object%5D&name=image.png&originHeight=796&originWidth=1318&size=346588&status=done&style=none&width=659)
> 点击**Actions -> Trust Root Certificate**，为电脑安装证书：

![image.png](https://cdn.nlark.com/yuque/0/2020/png/97322/1607129024738-0e8cc53f-f0d7-4bd4-a3e0-763aeef2cfed.png#align=left&display=inline&height=531&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1062&originWidth=2306&size=1018003&status=done&style=none&width=1153)<br />- 点击Yes<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/97322/1607129038225-467c1068-59e4-4a57-a992-c9797a018c46.png#align=left&display=inline&height=466&margin=%5Bobject%20Object%5D&name=image.png&originHeight=932&originWidth=1630&size=713085&status=done&style=none&width=815)<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/97322/1607129050438-56b511ff-c109-486e-beb7-8b7811732e41.png#align=left&display=inline&height=443&margin=%5Bobject%20Object%5D&name=image.png&originHeight=886&originWidth=1374&size=480490&status=done&style=none&width=687)<br />这样就在电脑端装好了证书<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/97322/1607129064515-8ff21cc7-e2e2-4f97-8ee8-153d62921c29.png#align=left&display=inline&height=417&margin=%5Bobject%20Object%5D&name=image.png&originHeight=834&originWidth=1338&size=408319&status=done&style=none&width=669)

---

- 配置允许远程电脑连接（这样就可以抓手机的包了）
> 在Options的主面板中，点击 Connections，设置连接规则等。包括端口号的设定，一定要记得选中**允许远程电脑连接**，我们就可以使用这个作为手机的代理，从而抓取手机的包了。

![image.png](https://cdn.nlark.com/yuque/0/2020/png/97322/1607129081900-168e6985-0b03-4ae4-b873-e4d0cc063c91.png#align=left&display=inline&height=422&margin=%5Bobject%20Object%5D&name=image.png&originHeight=844&originWidth=1330&size=457443&status=done&style=none&width=665)

- 后面的话使用**默认的配置**就可以了
<a name="gqh02"></a>
# 二、手机设置
<a name="aR9kj"></a>
## 1. 抖音版本选择
试了好多版本的抖音，发现6.3.0版本的最好抓包，所以我就使用了**6.3.0版本**的抖音，大家如果需要的话可以关注公众号获取**安装包**。

- 安装好抖音之后，记得不要更新，也可以把应用市场的自动更新禁掉。
<a name="sPoym"></a>
## 2. 配置手机网络
<a name="UWsz9"></a>
### 2.1. 保证手机和电脑在同一个局域网内
使用同一个路由器下的网络就行，学校内网应该也是可以的，或者没有路由器的话，用另一个手机开热点给它俩连也可以<br />![](https://cdn.nlark.com/yuque/0/2020/png/97322/1607128935407-c677b55b-98bf-42f5-85b2-73c1e38a74bf.png#align=left&display=inline&height=131&margin=%5Bobject%20Object%5D&originHeight=131&originWidth=1067&size=0&status=done&style=none&width=1067)
<a name="44rFL"></a>
### 2.2. 设置手机代理

- 首先查看电脑的ip<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/97322/1607129098299-0f463ef1-0aa9-4e42-ac69-576a1a47b5b1.png#align=left&display=inline&height=397&margin=%5Bobject%20Object%5D&name=image.png&originHeight=794&originWidth=1850&size=273068&status=done&style=none&width=925)
- 设置手机代理

![image.png](https://cdn.nlark.com/yuque/0/2020/png/97322/1607129121381-d0c65070-6f98-48f3-96ea-f7064ebe4e71.png#align=left&display=inline&height=602&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1204&originWidth=2604&size=783031&status=done&style=none&width=1302)<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/97322/1607129139580-191ef732-339e-4550-b486-b49e32acc7f0.png#align=left&display=inline&height=590&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1180&originWidth=1590&size=396266&status=done&style=none&width=795)<br />这个时候手机代理就设置好了，如果以上步骤都没有问题的话，这个时候应该已经可以联网了，可以用手机上一下百度，测试一个，如果不可以联网，检查一下你的手机网络代理设置是不是正确的：（电脑ip正确不，前面设置的Fiddle的Options里面的Connetions里面的端口是不是和手机上设置的一样），如果没问题，建议重启一下手机，我的手机连不上网的时候重启一下就好了，然后连接网络，然后就可以上网了。

- 安装证书

因为要爬HTTPS 的包，所以需要安装证书，前面已经知道了你的电脑的ip地址，还有fiddle中设置的端口号，在手机浏览器中输入：**http://电脑ip:端口号**，例如你的电脑的ip是192.168.0.1，设置的端口号是：8888，那么你就要输入：[http://192.168.0.1:8888](http://192.168.0.1:8888)<br />如果上一步你的代理设置成功了，那么就会出现这个页面：<br />点击下载证书，然后安装，过程如下：<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/97322/1607129154935-d7b6d9f5-9467-4245-90c3-2e9f9c19ee69.png#align=left&display=inline&height=383&margin=%5Bobject%20Object%5D&name=image.png&originHeight=766&originWidth=2546&size=519336&status=done&style=none&width=1273)<br />到这里手机就安装好证书了，这个时候打开抖音，我们可以看到Fiddle已经可以抓到抖音的数据包了<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/97322/1607129172464-c579583d-7141-4d39-ad6d-2b8050c0c111.png#align=left&display=inline&height=685&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1370&originWidth=2836&size=2141680&status=done&style=none&width=1418)<br />上面的图就是抖音某用户发布的视频的抓包，我们可以通过分析请求头以及对应的响应获取我们想要的数据了。<br />
<br />——————————————————————————————————————————
<a name="9794cc28"></a>
#### TiToData：专业的短视频、直播数据接口服务平台。
<a name="1c5f89ff"></a>
#### 更多信息请联系： [TiToData](https://www.titodata.com?from=douyinarticle)
覆盖主流平台：抖音，快手，小红书，TikTok，YouTube
