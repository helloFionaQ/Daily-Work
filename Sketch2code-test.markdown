# 对Sketch2code简单的测试和相关资料的阅读 
##  Sketch2code的简介和小测试 ##
1. 如下图使用经典的Sketch2code将手绘图像转换为HTML的过程：
![](https://mmbiz.qpic.cn/mmbiz_gif/kOTNkic5gVBGxKSz2WJQm5LOgdTHGGgCicP9DC2H0Rhf8fezYSHKX8GWoCglt9lhoc7qo5ts5Q3toPJx7PibfqGww/640?wx_fmt=gif&wxfrom=5&wx_lazy=1)                

 ● 用户首先要把图片上传到网站上。

 ● 自定义视觉模型可预测图像中存在的HTML元素，并确定其位置。

 ● 手写文本识别服务读取预测元素内的文本。

 ● 布局算法通过预测元素边框的空间信息生成可适应所有这些组件的网格结构。

 ● HTML生成引擎，使用以上信息来生成最终结果的HTML代码。

2.通过上图简单的理解，对上面的图像界面的测试

   测试用例：如上图

   测试结果：与设计者所提供的设计效果近似一致。包括文本框的显示和文字的使用效果都很美观。

3.实验的不足：

   此次只是对其课题的简单理解，没有对它的构造原理等做详细的理解，下次从此方面下手，并且多观测一些图像的转化。






