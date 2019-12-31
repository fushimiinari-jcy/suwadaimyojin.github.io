### 这是一个基于 Vue 开发的东方 project 视频索引网站

域名： **[www.patchyvideo.com](www.patchyvideo.com)**

目前上线的版本基于 flask 框架开发，网站正常运作。

用户可登陆注册上传修改视频，以及对 Tag 的增删改除

> 完整项目详情可移至 [https://github.com/zyddnys/PatchyVideo](https://github.com/zyddnys/PatchyVideo)项目仓库查看
>
> >

感谢 zyddnys 的开源提供的后台接口，因目前本项目已经变成多人协作项目，需要详细开发流程进度，故在此标注

网页大致分为九个区域

- Home √
- Deatil(Video) √
- Playlists √
- Detail(Playlists) √
- Create Playlists ×
- Post Video X
- Tags X
- Login \ Sign Up √
- Users X

#### X:无进度

#### √:待完成

---

### 项目技术架构

插件：

- vue/cli-service
- vue/cli-plugin-babel
- vue/cli-plugin-router
- vue/cli-plugin-vuex
- vue/cli-plugin-element
- vue-infinite-scroll
- stylus
- jquery
- webpack
- font-awesome

项目依赖：

- core-js
- element-ui
- vue
- vue-router
- vuex

开发依赖

- vue-temmplate-compiler

---

### 具体实现——

一、Home：

1.数据的渲染  
2.分页功能实现  
3.element-ui 排序美化

二、Deatil(Video & Playlists)

1.数据的渲染  
2.各个链接间的通道

三、Playlists

1.数据的渲染  
2.分页功能实现  
3.element-ui 排序美化

三、LogIn / Sign Up

1.路由守卫  
2.element-ui 图标美化  
3.LogIn 表单验证功能  
4.登录成功失败状态提示、登录功能实现

---

### 需要完善——

一、Home：

1.点击相应的 Tags 渲染筛选出的视频  
2.导航栏处 Search 功能的实现

二、Deatil(Video)

1.点击相应的 Tags 渲染筛选出的视频  
2.Edit Tags 样式位置调整
3.Copies 和 Playlists 区的功能完善

三、Playlists

1.指向列表作者的链接尚未完工  
2.由于标题可能会超过一行导致视频列表高度变高，从而导致排版不太好看

四、Detail(Playlists)

1.播放列表里链接的复制功能因为涉及到对 dom 的直接操作，所以可能会有被抓住漏洞的风险

五、Login \ sign Up

1.利用本地储存确保登录信息保留可能会导致信息不安全  
2.sign Up 界面的 Email 格式校验功能有待完善

---

### 用到接口——

日后会专门整理接口文档

---

### 注意的点

实际开发中可能有多处考虑不周，设计模式上存在缺陷。还请多多包涵。如觉得本方案不适用可自废另起新路。

一、链接复制功能

因为使用了 jQuery 对 dom 进行直接操作，所以可能会增加被入侵的风险

二、本地储存功能

为了保证登录状态在网站被刷新/出现打开的时候不被刷新，网站利用本地储存对用户名和登录状态进行了储存

isLogin: true 表示登录状态，false 表示未登录状态

username: 储存的用户名

在页面渲染的时候会对这两个数值进行调用以确定用户的登录状态

但是这样可能会增加被入侵的风险，所以以后维护代码的时候需要多多注意这个地方

---

### 写在最后

一、

网站在初期建设时，我刚结束 JS 部分的学习。  
起初群里招人时，似乎没人愿意胜任这份无薪酬的工作。  
我抱着学习尝试的态度加入了只有两人的开发群，
非常感谢 zyddnys 允许一个毫无经验的初学者来参与他的网站建设。  
zyddnys 最初的设计理念是偏向 Danbooru、 Gelbooru 风格的。  
我也是将他最开始的布局延展至今。

遗憾的是以我现有的拙劣水平尚不能穷尽这些美。  
从开始的茫然到制作的喜悦。
从两人的寂静到诸位的热闹。

我见证了从最初的两人演变至现在的三十八人。
我见证了宣传后的人们一齐涌入的热情。
我想我唯一的作用是让它稍微能入人眼目了，能让更多优秀的人寻着它，给它灿灿地生光、蓬勃地奋飞。

日新之谓盛德,生生之谓易

希望 patchyvideo 能留住这些好的故事

written by suwadaimyojin

二、

说起来，自己认识东方才大概一年的时间。  
曾几何时，受到一些前辈的影响，“为东方做出一些自己的贡献”，这种想法愈加强烈。  
自己也一直在把这种想法付诸实现。

但是，在十月的时候，在和一个游戏社团的主催的矛盾终于无法弥合的时候，自己选择了退出。  
那件事带来的伤痛，至今难以消除。  
但是自己，也从没放弃过自己的追求。

或许十年后的自己回过头来看自己今天所作的选择，会感到一丝遗憾吧，  
在考研前一个月，在考研最紧张的复习阶段，选择加入到网站开发中来。  
不过，自己绝不后悔自己所做出的选择，  
因为，它在自己心里已经比考研更加重要了。

重新拾起 vue，或许还能凭着自己以前的开发经验，为东方做些什么，自己是这么想的。  
虽然前辈们的背影离自己是那么的遥远，但这从来不是松懈的理由。  
用 vue 重构网站的过程并不是一帆风顺，很多时候会遇到各种各样奇怪的问题，但自己坚信，现在的努力，是不会没有意义的。  
曾经 vocaloid 的粉丝们用自己的双手搭建出了 Mikufans，东方的粉丝们也一定可以做到同样的事情，甚至做的会更好。
如果每一个东方众都为东方做出自己的贡献的话，东方就会永远向前。  
游戏王圈里的前辈们教会了自己这个道理，希望大家也能一起向前，不仅仅是 patchyvideo，还有所有的，东方的回忆，  
都能被永远的铭记。

written by wrzrmzx(freesia)
