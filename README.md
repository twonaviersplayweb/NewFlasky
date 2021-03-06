#序章
###如何学习FLASK
####一 历史回顾
又要开始一轮 Impossible Mission了!如何才能把mission accomplish 呢.按照以往的做法肯定是这样的，一开始雄心壮志，新鲜感十足的去学习第一章，然后发现太简单，代码逗懒得抄完酒迅速的往下翻，巴不得一晚上就掌握。然后就突然遇到一个不会的地方了，此时信心大挫，但是也没去分析究竟哪里不会，就急匆匆的往下看希望跳过不会的地方，草草的翻了一遍后发现，偏偏就是这一章过后，难度好像陡然上升，后面往竟然一点都看不懂，然后往就把这个东西放到一边去了，接着去发掘另外一个简单的能让我**轻轻松松**学好的东西了，你以为故事这就结束了嘛，不是的精彩还在后面呢。

学了一圈过后，都是同样的轮回，我可能一圈的学不会又绕回来了，没记错的话这是我第三次准备学flask了，同一本书，第一部分我已经看了2遍了，而后面的第二三部分我还没有看过，按照传统这次我就要看第三遍了，然后我估计我又快放弃了！对了这次可能不会放弃，我可能会最终像模像样的抄完，因为我实在无力支付1000元，穷啊！
####二 总结教训
为什么会这样？学什么都失败，都不成功，都眼高手底，简单的做不好，难的做不来。从以前的经验来看，我学什么都是同一套逻辑，图快想一步到位瞬间学会，期望值及其的高，高到令人发指，遇到一丁点的挫折心理就有落差，总是想找一个不用动脑子的，不累的，不折腾的方法跨过挫折，没有的话就放弃，什么分析啊，逆推啊，层层剥丝抽茧，最终解决问题就没在我身上看到过，即使有的解决了，也是我侥幸花了大量时间盲目尝试出来的，没有任何章法可循。

对于不肯动脑子，不肯去理解，折腾，总是一味求快求顺利的人来说，我只想用二十六年惨痛的经验告诉你，这种心态事搞不出什么名堂来的，也学不会什么东西，不思考永远被牵着走，没有自我。

####三 该怎么办
先端正态度，然后再对可能发生的意外情况进行提前准备一套预案
#####[态度]()
* 虽然17天看完这本书是拍脑袋说能完成的，但是这逼装下来了，就要把它圆了，这是从今天开始到10月8号这段时间里最重要的事情，优先级最高！
* 看完了基本就涅槃了，创造你的世界里面的记录了
* 完不成就又把自己往重复的生活中推了
* 这是对自己的承诺，虽然不用承担什么严重后果。但是总是失信于自己，又怎么相信自己可以改变自己的命运呢
* 一定会遇到不会的地方，与自己预期不一致的地方，这时候要客观不要害怕，不要不敢面对，没有什么难的

#####[方法预案]()
* 首先用书的页数除以天数，然后规定自己每天看的页数，这个方法肯定是必败无疑，因为从来没成功过，NEVER!
* 按照书上划分的几个部分，对照着别人博客的效果，然后自己思考该如何实现，如果能实现就先实现，不能实现也要想将怎么流程理出来，然后再去看书上对应的部分是如何实现的
* 遇到不会的错的，要及时的提醒自己开始分析，不要慌乱尝试乱猜，要有计划有记录的调试问题。
* 遇到不会的问题，先口头描述一遍或者写在纸上
* 思考一下FLASK是什么，用来干什么，设计的理念是什么，是属于什么类型的MVC框架，它的哪些设计体现了这一思想
* 多用思维导图，多逆推

------

#今天的计划
> * 整理出一个博客需要包含哪些部分
> * 思考一下FLASK究竟是什么，干什么用的
> * 列一下本周计划


#初章
###Flask 是什么
今天看了一些关于wsgi的东西，WSGI的全称是Web Server Gateway Interface，翻译过来就是Web服务器网关接口。具体的来说，WSGI是一个规范，定义了Web服务器如何与Python应用程序进行交互，使得使用Python写的Web应用程序可以和Web服务器对接起来。

WSGI相当于是Web服务器和Python应用程序之间的桥梁。那么这个桥梁是如何工作的呢？首先，我们明确桥梁的作用，WSGI存在的目的有两个：

- 让Web服务器知道如何调用Python应用程序，并且把用户的请求告诉应用程序。

- 让Python应用程序知道用户的具体请求是什么，以及如何返回结果给Web服务器。

Flask扮演者python应用程序的角色，也就是通常所说的框架，框架只干一件事情，**处理客户的请求，只需要关心业务逻辑部分**，至于返回http的请求，这些由服务器去完成。而client的请求基本上都是数据相关的，一切都围绕着数据展开。


###博客包涵哪些部分
书里已经讲的非常清楚了，
> * 用户认证
> * 用户角色
> * 用户资料
> * 博客文章
> * 关注者
> * 用户评论
> * 应用程序接口

这些都是一些博客需要的功能，因为需求而产生的。当往写这些的时候我希望自己能够好好思考一下，这些功能的由来，需求来自何方，然后再去实现，而不是一味的去抄。有一个思考的过程，为什么会有这些功能，如果没有回怎么样。

书上页面使用jinja2模版，数据库为sqlite3，关于jinja2我感觉展示页面不错，代码也不多，语法也简单。但是我将使用angular ＋ bootstrap 来制作页面。angualr的双向数据绑定用起来实在太酸爽了，根本停不下来，而且可以干很多需要flask扩展件干的事情。可以少写不少python代码。

数据库的选择上我使用mongodb。主要关系型数据库一直不得窍门，加之sql语句我觉得太长难记，数据提取出来的时候还要做很多处理，而mongo天生支持json，插入数据使用起来比较方便而且语句比较短，而且检索的数据基本直接就可以使用

如果有时间的话我希望 我能用jinja2 ＋ sqlite3 再实现一遍，和angular ＋ mongo 做一个对比，找出彼此的优劣


###明天计划
- 将第五章的数据库部分由sqlite3 转换成mongodb
- 将第四章的表单部分用angular来实现




