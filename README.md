# 苏燕鲁的简历

## 先讲讲怎样才是一份好的技术简历

首先，一份好的简历不光说明事实，更通过FAB模式来增强其说服力。

 - Feature：是什么
 - Advantage：比别人好在哪些地方
 - Benefit：如果雇佣你，招聘方会得到什么好处 

其次，写简历和写议论文不同，过分的论证会显得自夸，反而容易引起反感，所以要点到为止。这里的技巧是，提供论据，把论点留给阅读简历的人自己去得出。放论据要具体，最基本的是要数字化，好的论据要让人印象深刻。

举个例子，下边内容是虚构的：

2006年，我参与了手机XX网发布系统WAPCMS的开发（```这部分是大家都会写的```）。作为核心程序员，我不但完成了网站界面、调度队列的开发工作，更提出了高效的组件级缓存系统，通过碎片化缓冲有效的提升了系统的渲染效率。（```这部分是很多同学忘掉的，要写出你在这个项目中具体负责的部分，以及你贡献出来的价值。```）在该系统上线后，Web前端性能从10QPS提升到200QPS，服务器由10台减少到3台（``` 通过量化的数字来增强可信度 ```）。2008年我升任WAPCMS项目负责人，带领一个3人小组支持着每天超过2亿的PV（``` 这就是Benefit。你能带给前雇主的价值，也就是你能带给新雇主的价值。 ```）。

有同学问，如果我在项目里边没有那么显赫的成绩可以说怎么办？讲不出成绩时，就讲你的成长。因为学习能力也是每家公司都看中的东西。你可以写你在这个项目里边遇到了一个什么样的问题，别人怎么解决的，你怎么解决的，你的方案好在什么地方，最终这个方案的效果如何。

具体、量化、有说服力，是技术简历特别需要注重的地方。

（以上内容在写完简历后，对每一段进行评估，完成后再删除）

---


# 联系方式
（HR会打印你的简历，用于在面试的时候联系，所以联系方式放到最上边会比较方便）

- 手机：13815890625
- Email：suyanlu@gmail.com
- QQ/微信号：325189/yanlusu

---

# 个人信息

 - 苏燕鲁/男/1979 
 - 本科/南京航空航天大学计算机系 
 - 工作年限：15年
 - 技术博客：http://www.iwankr.com
 - GitHub: https://github.com/wscsm

 - 期望职位：Android高级程序员，应用架构师
 - 期望薪资：税前月薪15k~20k，特别喜欢的公司可例外
 - 期望城市：南京
 - 期望工作方式：Home Office

---

# 工作经历
2015年至今：北京明智科技有限公司
2014年至2015年：玺时资产管理有限公司
2001年至2013年：华为技术有限公司

## 北京明智科技有限公司 （ 2015年2月 ~ 2016年 ）

### 家信项目 
该项目给家庭成员提供实时分享功能的app，概念取自“一封家书”，主打家庭关系交流。

我在此项目中负责android客户端的开发工作，北京方面在80%完成的时候将ios客户端代码交给我，我负责把ios客户端的UI和逻辑在android上实现。

其中做的较为出色的是自定义照片墙展示视图，把ios上能够轻松实现的图片处理（包括照片缩放、视图内照片拖移、视图转场动画等技术难点）在android上面实现，展示的效果和ios上相比能达到90+%的相似度

遇到的最大的困难也是自定义照片墙视图，该视图可以展示多张照片，又不同于通用的相册，其中的多张照片的显示大小是不一样的，有一顶的规律，也不能套用flow式样，不同的照片要可以交换位置，交换过程中要有自然的动画过渡，涉及到了自定义视图动态布局、拖拽、动画以及图片缩放缓存方面的处理细节很多，因此实现起来相对也比较复杂，最终实现的效果和ios上的相差很小，尤其在拖拽照片交换位置这方面，北京的同事表示android上面能做到这样真的很不错:)

### 健身教练项目
给健身教练和客户之间建立关系的一个应用，技术难点在于小视频的录制、播放以及android和ios的数据一致性，android和ios所用的视频标准不完全一样，因此在将ios的视频逻辑移植到android上的时候非常麻烦，UI的表现不能差太多，视频的各种参数要能兼容，需要考虑的问题非常多。

最开始考虑模仿微信的小视频来做，经过一段时间研究发现：微信的小视频录制用的是ffmpeg定制，微信精简了ffmpeg，只保留了视频流录制和视频转gif部分的功能，反编译微信的apk后可以发现在聊天界面展示的无声音小视频是high quality gif而不是视频（所以没有声音但是又比较清晰），点开后全屏播放就是视频了，但是要在短时间内对ffmpeg进行精简对一个外包项目来说是得不偿失的，因此最后采取了妥协的方案，编译了ffmpeg的android动态库，利用JNI直接进行命令行调用，固定视频的裁剪和转换命令，也可以达到小视频录制的效果，缺点就是耗时较长，后来发现秒拍（vitamio）的小视频也是采取的先录制后处理方式，不同的是他们也对ffmpeg进行了精简定制，所以他们的处理时间缩短了。


### 其他项目

广州本田4S店汽车展示app：该项目用了开源的panoramagl进行汽车的全方位立体展示，将汽车各个方位的照片进行预处理，再用panoramagl在app中展示出来，这个项目难题在于panoramagl开源代码的使用，其中的参数需要一点点的进行微调，达到一个比较好的效果。
 
## 玺时资产管理有限公司 （ 2014年1月 ~ 2015年1月 ）

### 公司IT设施组建项目 
我在此项目负责了哪些工作，分别在哪些地方做得出色/和别人不一样/成长快，这个项目中，我最困难的问题是什么，我采取了什么措施，最后结果如何。这个项目中，我最自豪的技术细节是什么，为什么，实施前和实施后的数据对比如何，同事和领导对此的反应如何。


## 华为技术有限公司 （ 2001年7月 ~ 2013年12月 ）

### AAA项目 
我在此项目负责了哪些工作，分别在哪些地方做得出色/和别人不一样/成长快，这个项目中，我最困难的问题是什么，我采取了什么措施，最后结果如何。这个项目中，我最自豪的技术细节是什么，为什么，实施前和实施后的数据对比如何，同事和领导对此的反应如何。


### 视频监控项目 
我在此项目负责了哪些工作，分别在哪些地方做得出色/和别人不一样/成长快，这个项目中，我最困难的问题是什么，我采取了什么措施，最后结果如何。这个项目中，我最自豪的技术细节是什么，为什么，实施前和实施后的数据对比如何，同事和领导对此的反应如何。

### IPTV项目 
我在此项目负责了哪些工作，分别在哪些地方做得出色/和别人不一样/成长快，这个项目中，我最困难的问题是什么，我采取了什么措施，最后结果如何。这个项目中，我最自豪的技术细节是什么，为什么，实施前和实施后的数据对比如何，同事和领导对此的反应如何。

---

# 其它作品
（这一段用于放置工作以外的、可证明你的能力的材料）

## 开源项目
（对于程序员来讲，没有什么比Show me the code能有说服力了）

 - [STU](http://github.com/yourname/projectname) : 项目的简要说明，Star和Fork数多的可以注明
 - [WXYZ](http://github.com/yourname/projectname) : 项目的简要说明，Star和Fork数多的可以注明

## 技术文章
（挑选你写作或翻译的技术文章，好的文章可以从侧面证实你的表达和沟通能力，也帮助招聘方更了解你）

- [一个产品经理眼中的云计算：前生今世和未来](http://get.jobdeer.com/706.get)
- [来自HeroKu的HTTP API 设计指南(翻译文章)](http://get.jobdeer.com/343.get) （ ```好的翻译文章可以侧证你对英文技术文档的阅读能力```）

## 演讲和讲义
（放置你代表公司在一些技术会议上做过的演讲，以及你在公司分享时制作的讲义）

  - 2014架构师大会演讲：[如何通过Docker优化内部开发](http://jobdeer.com)
 - 9月公司内部分享：[云计算的前生今世](http://jobdeer.com)

# 技能清单
（我一般主张将技能清单写入到工作经历里边去。不过很难完整，所以有这么一段也不错）

以下均为我熟练使用的技能

- Web开发：PHP/Hack/Node
- Web框架：ThinkPHP/Yaf/Yii/Lavaral/LazyPHP
- 前端框架：Bootstrap/AngularJS/EmberJS/HTML5/Cocos2dJS/ionic
- 前端工具：Bower/Gulp/SaSS/LeSS/PhoneGap
- 数据库相关：MySQL/PgSQL/PDO/SQLite
- 版本管理、文档和自动化部署工具：Svn/Git/PHPDoc/Phing/Composer
- 单元测试：PHPUnit/SimpleTest/Qunit
- 云和开放平台：SAE/BAE/AWS/微博开放平台/微信应用开发

## 参考技能关键字

本技能关键字列表是从最近招聘Android的数百份JD中统计出来的，括号中是出现的词频。如果你的简历要投递给有机器（简历分选系统）和不如机器（不懂技术的HR）筛选简历环节的地方，请一定从下边高频关键词中选择5～10个适合你自己的。

- android(1830)
- java(386)
- ui(180)
- app(178)
- http(149)
- sdk(135)
- tcp(95)
- socket(93)
- api(60)
- xml(48)
- framework(48)
- eclipse(41)
- linux(38)
- json(28)
- ndk(27)
- ios(27)
- sqlite(26)
- andriod(25) 2%的HR把android给写错了 T_T
- html5(25)
- web(23)
- github(21)
- jni(20)
- svn(15)
- gui(14)
- git(13)
- wifi(10)
- 3g(10)
- j2me(10)
- mysql(10)
- oracle(9)
- html(9)
- sql(8)
- tv(8)
- mvc(8)
- lbs(8)
- code review(7)
- im(7)
- mobile(6)
- view(6)
- stackoverflow(6)
- xmpp(6)
- o2o(5)
- ue(5)
- objective(5)
- js(5)
- blog(5)
- andorid(5)
- rom(5)
- launcher(5)
- restful(5)
- webservice(4)
- apk(4)
- androidsdk(4)
- oo(4)
- javascript(4)
- j2ee(4)
- opengl(4)
- uml(4)
- sms(3)
- windows(3)
- market(3)
- audio(3)
- httptps(3)
- udp(3)
- store(3)
- php(3)
- unity3d(3)
- native(3)
- webview(3)

---

# 致谢
感谢您花时间阅读我的简历，期待能有机会和您共事。
