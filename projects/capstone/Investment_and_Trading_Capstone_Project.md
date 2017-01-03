投资交易毕业项目

创建一个股票价格指标

# 描述

投资公司、对冲基金甚至个人都在使用金融模型来更好地理解市场行为，做出有回报的投资和交易。大量的信息以历史股价和公司业绩数据的形式存在，这也适合机器学习算法来处理。

对于这个项目，你的任务是创建一个股价指标，获取一段特定日期范围内的每日交易数据作为输入，输出给定查询日期的预计估算。注意输入会包含多个指标，比如开盘价（Open），最高成交价（High），股票交易数量（Volume）以及股票分拆和股息后的已调整收盘价（Adjusted Close）；你的系统只需要预测已调整收盘价。

你可以自由选择你的项目的形式（简单的脚本、web应用/服务、Android/iOS应用等），以及选择任何你想要的添加/改动（比如，建议做什么交易）。
务必在你的文档中记录你既定的功能。

# 设置

简单脚本或web应用/服务的推荐设置：

*   Python
*   NumPy, SciPy, Pandas
*   （可选）数据访问的Python API（见下）

Android/iOS app:

*   Android/iOS SDK
*   数据访问的原生库/API（见下）

# 数据

这里有几个可以自由使用的开源历史股价数据

*   [Yahoo! Finance](http://finance.yahoo.com/): 你可以通过web API直接查询一支股票，或者下载.csv的dump文件使用。
*   [Bloomberg API](http://www.bloomberglabs.com/api/libraries/): 多种API可用，包括Python。
*   [Quandl](https://www.quandl.com/home-v3): 同样多种API可用，包括Python。

查找可以让你获得每日股价，如Open，High，Low，Close，Volume以及Adjusted Close的API endpoint/库函数。记住Adjusted Close是你要预测的。

# 任务

## 实现股票预测程序

你的核心股票预测要实现：

* 一个训练接口，接受日期范围（start_date, end_date）和股票代号（如，GOOG，AAPL），创建一个股票操作行为的模型。你的代码应从你选择的数据源读取想要的历史价格。
* 一个查询接口，接受一个日期的列表和一个股票代码的列表，输出那些股票中的每一支在给定日期的预测股价。注意传入的查询日期必须是在交易日期范围之后，股票代码必须是训练集的子集。

## 测试和评估性能

一个核心系统的基本运行会用到一次训练接口的调用，一次或多次的查询接口的调用。实现一个训练-测试循环来评估你的模型的性能。用它来测试在训练的结束日期后，对于不同间隔的查询日期中的预测准确度，比如训练的结束日期后的下一天，7天后，14天后，28天后等等。

（注意：相应地选择训练阶段，以便你有未来许多天的基本的真实数据。）

## 创建用户接口

一旦你的股票预测程序迭代了几次后，它能给出你满意的结果（比如说，7天的预测股价平均误差在实际值的+/-5%内），实现一个更友好的接口，可以让你指定你感兴趣的股票并准备一些预设的时间段。


你可以扩展系统来建议适合买或卖的股票，以及何时买卖。你也可以为用户维护一个股票投资组合，来使得建议更具体。在你的报告里用图、截屏等来体现这些功能提升。

# Rubric

对于评价你的提交项目的各个部分的标准，请参考[毕业项目评价标准](https://docs.google.com/document/d/1Z2y5Kg4l6xKG_QRRukFYipDUqQc5gt9t6d1EBrE632U/pub?embedded%3Dtrue)。

# 成果物


请提交下列文件，最好压缩为单个压缩包：

*   所有项目需要的代码。
*   一个README文件，标题为“创建一个社交图片的描述平台”，连同运行代码的指导。
*   项目报告，一个.PDF文件。

你的项目文档应该遵照类似于[毕业项目](https://www.udacity.com/course/viewer%23!/c-nd009/l-5420178917/m-5479829792)和[项目模板](https://docs.google.com/document/d/1B-vEOscvfqctGEMHTFDS9Nw7aqcE2iuwPRfp0jK8nf4/pub?embedded%3Dtrue)中提及的结构。

# 学习资源

## 课程

*   [Machine Learning for Trading](https://www.udacity.com/course/machine-learning-for-trading--ud501), Tucker Balch (Georgia Tech and Udacity)
*   [Stocks and Bonds](https://www.khanacademy.org/economics-finance-domain/core-finance/stock-and-bonds), Khan Academy

## 书籍

*   [Python for Finance](http://python-for-finance.com/), Yves Hilpisch
