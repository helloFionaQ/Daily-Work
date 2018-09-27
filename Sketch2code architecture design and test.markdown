# Sketch2code architecture design and test #


## Sketch2Code architecture design ##



1. Sketch2Code 使用了以下组件：  

•微软自定义视觉模型（Custom Vision）：这个模型是基于不同的手绘稿的图象训练得出的，并标记了与常见 HTML 元素（如文本框、按钮、图像等）相关的信息。


•微软计算机视觉服务：用于识别设计元素中的文本。


•Azure Blob Storage：保存与 HTML 生成过程的每个步骤相关的信息，包括原始图像、预测结果、布局和分组信息等。


•Azure Function：它作为后端入口点，通过与其他服务发生交互来协调生成过程。


•Azure Website：用户界面前端，用户可以在这里上载设计图，并查看生成的 HTML。

## Sketch2code test ##
1. 
测试用例一：

   ![](http://a2.qpic.cn/psb?/31c73372-bbf1-44a2-a0ef-d40393026b98/9z*srDdgKb8vBZWs19u4s.Y0WvschY837lKSLSmdos4!/m/dD0BAAAAAAAA&bo=OASgBQAAAAARB6k!&rf=photolist)

 测试结果一：

![](http://a2.qpic.cn/psb?/31c73372-bbf1-44a2-a0ef-d40393026b98/fnkpr2R5gfS29QZDtO1J0uv0Ru285RBlgkz1OZzTa.o!/m/dN0AAAAAAAAA&bo=XQRqAgAAAAARBwE!&rf=photolist)

第一次用自己的中文图形进行测试未出现其对应的HTML代码

2.
测试用例二：

![](http://a4.qpic.cn/psb?/31c73372-bbf1-44a2-a0ef-d40393026b98/nyTHeqXewfnzg.BNHejT63r4*Y*Ab7vEpSsGJj*frt8!/m/dOsAAAAAAAAA&bo=oAU4BAAAAAARB6k!&rf=photolist)

测试结果二：

![](http://a1.qpic.cn/psb?/31c73372-bbf1-44a2-a0ef-d40393026b98/SpTBIuaTCB1H8ExWaks.joOgxb4kTLolYfHJBnWr2A0!/m/dOAAAAAAAAAA&bo=LQRWAgAAAAARB00!&rf=photolist)

第二次用自己的英文图形进行测试未出现其对应的HTML代码

3.测试结果分析：

刚开始想希望用自己的图形来测试其的有效性发现没有出现期望的HTML，然后对应于example可能猜想由于中文的字样的出现，后来用图二进行测试发现也没有出现HTML的代码，所以测试结果不太理想，我猜测是由于字体颜色导致的，下次测试再用改变一下，希望看可以出现预期的html代码。
