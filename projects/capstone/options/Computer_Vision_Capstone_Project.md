机器视觉毕业项目

创建一个社交图片的描述平台

# 描述

创建一个社交图片的描述平台。用户可以上传一张想要被描述的图片，然后图片就显示在其他用户的消息流上，一个或多个用户能描述这张图片。
久而久之，系统学习了描述图片的语言与其视觉特征的关联，然后自己能更好地预测描述。

你可以用几个不同方法中的一个（或组合），来从图片中收集信息，包括（但不仅限于）：

*   视觉词袋
*   Gist
*   SIFT，SURF或其他本地的特征描述符号
*   形状空间

为了标记，你可以把描述当作一个简单的词袋来处理。更高级的模型的话，可以把一个用户输入的描述字符串解析出来，并理解句子的结构和语法，之后可以生成出听上去比较自然的描述。

# 设置

如果你要创建一个桌面应用/程序，或者一个web应用：

*   [机器视觉开发的设置和参考](http://cn-static.udacity.com/mlnd/capstone/CVDevSetupandReferenceMaltabOctavePython.html)（遵照Python的说明）
*   Clone并安装这个库：[Lumos](https://github.com/napratin/lumos)
    玩一下这个库，从[README](https://github.com/napratin/lumos/blob/master/README.md%23installation-and-usage)的样例代码中创建一份拷贝，然后改动一下做些有意思的事情。务必使它按照期望运行；
    你应该能够调用它来处理从命令行输入的视频或静态图片文件，或者处理摄像头的数据流（默认）。

如果你要创建一个Android或者iOS的应用，你可能会用OpenCV。
[Android](http://opencv.org/platforms/android.html)/[iOS](http://docs.opencv.org/2.4/doc/tutorials/introduction/ios_install/ios_install.html)
也许你只会用到原生的功能，又或者你还会用到其他通用库——这完全取决于在实现中用了什么算法（以及用了多少）。

# 任务

利用下列说明作为完成项目的指导方针。务必在报告中包含了所有给定的问题/提示。

1.  选择一个目标平台（桌面/web/Android/iOS），设计完整的应用程序。将它描述为你创建一个验证概念的产品，完成用户界面的设计（很简单的模型也可），预期的使用范围和功能。
2.  清晰说明在你应用中的机器视觉/机器学习模块，包括输入、期待的输出和你考虑的一些算法。
3.  首先创建系统面向用户的部分，包括上传图片的方法，在一个用户的消息流/主页中展示未标记的图片，保存输入的描述。在你的报告中加上系统的截图来说明使用场景和流程。
4.  准备训练和测试用的数据集，以便你可以重复（且可靠）地衡量你系统的表现。你可以用当前已建立的系统来创建数据集（可能需要你朋友的帮忙？！）。在报告中包含你的数据集的统计（图片数量，训练-测试划分等）。
5.  现在实现并测试你的图片描述匹配算法。你用了什么机器视觉和/或机器学习的技术？你用了什么测度指标来比较预测的描述和人类标记的描述？
6.  实现其他的功能，完成并改进你的应用。你最终的系统做了什么？与你最初构思的系统有多大的不同？对于见过的和没见过的样例，它的表现如何？


在你的报告里包含你在这个过程中有过的任何想法和反馈。还有重要的是，要注明运行代码所需的特殊依赖和说明。

# 评价标准

对于评价你的提交项目的各个部分的标准，请参考[毕业项目评价标准](https://docs.google.com/document/d/1Z2y5Kg4l6xKG_QRRukFYipDUqQc5gt9t6d1EBrE632U/pub?embedded%3Dtrue)

# 成果物

请提交下列文件，最好压缩为单个压缩包：

*   所有项目需要的代码。
*   一个README文件，标题为“创建一个社交图片的描述平台”，连同运行代码的指导。
*   项目报告，一个.PDF文件。


你的项目文档应该遵照类似于[毕业项目](https://www.udacity.com/course/viewer%23!/c-nd009/l-5420178917/m-5479829792)和[项目模板](https://docs.google.com/document/d/1B-vEOscvfqctGEMHTFDS9Nw7aqcE2iuwPRfp0jK8nf4/pub?embedded%3Dtrue)中提及的结构。

# 学习资源

## 课程

*   [Object Recognition and Scene Understanding](http://people.csail.mit.edu/torralba/courses/6.870/6.870.recognition.htm), Antonio Torralba (MIT)
*   [Introduction to Computer Vision](https://www.udacity.com/course/introduction-to-computer-vision--ud810), Aaron Bobick (Georgia Tech and Udacity)
*   [Introduction to Computer Vision](http://cs.brown.edu/courses/cs143/), James Hayes (Brown)

## 书籍

*   [Computer Vision: Algorithms and Applications](http://szeliski.org/Book/), Richard Szeliski
*   [Computer Vision: Models, Learning, and Inference](http://www.computervisionmodels.com/), Simon Prince
