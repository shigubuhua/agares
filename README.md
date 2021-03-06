# agares

agares目前是一个基于python的量化回测框架，其定位是帮助设计股市交易策略。虽然许多炒股软件中都有量化回测功能，它们的语法过于封闭，有很多表达限制。agares保留了python这门通用语言的所有功能。不仅可以导入K线数据进行技术分析，而且可以自行扩展接入其它数据如宏观经济数据，股民网络言论等，使得用户可以以大数据的思维，用机器学习，自然语言处理的算法对各种数据进行分析。

项目名阿加雷斯(agares)来自西方神话故事。阿加雷斯原指所罗门王72柱魔神中排第2位的魔神。据说他有能预见未来的能力，能道破世间的所有谜题，但是说出来的话却真假半掺，不能轻易相信。

目前，agares实现的基本功能有：

> * 使用tushare下载A股历史K线数据
> * 爬虫脚本爬取雪球网（知名投资网站）用户在某段时间内的发言
> * 提供strategy类：可根据buy和sell函数计算用户策略在历史上的performance
> * 提供analysis类：仅加载K线数据，用于与用户自行提供的各类数据做交叉分析

最后一个功能可能大家不太明白。其实这个类是用来实现agares的特色任务：用机器学习的算法对各类数据做分析。analysis文件夹提供了一个demo（Snowball\_comments\_analysis\_demo）给大家参考，抛砖引玉。在这个demo里，agares加载了雪球近几天的用户发言数据，分别用Nonnegtive Matrix Factorization（NMF）和Latent Dirichlet Allocation（LDA）算法提取了这几天的雪球股民们讨论的主题。

agares的代码比较简单，大家有兴趣的可以自己拓展。

使用说明：

https://github.com/ssjatmhmy/agares/blob/master/UserGuide.md
