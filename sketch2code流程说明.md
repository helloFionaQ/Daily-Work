Sketch2Code的使用流程
sketch2code 调查

---
首先，用户通过网站上传图像。
自定义视觉模型可预测图像中存在的HTML元素及其位置。
手写文本识别服务读取预测元素内的文本。
布局算法使用来自预测元素的所有边界框的空间信息来生成适应所有边界框的网格结构。
HTML生成引擎使用所有这些信息来生成反映结果的HTML标记代码。
![Sketch2Code工作流程][1]
Sketch2Code使用以下元素：

Microsoft自定义视觉模型：此模型已经过训练，其中包含不同手写设计的图像，用于标记最常见的HTML元素（如按钮，文本框和图像）的信息。
Microsoft计算机视觉服务：为了识别写入设计元素的文本，使用计算机视觉服务。
Azure Blob存储：存储 HTML生成过程中涉及的所有步骤，包括原始图像，预测结果和布局分组信息。
Azure功能：用作后端入口点，通过与所有服务交互来协调生成过程。
Azure网站：用户font-end，用于上传新设计并查看生成的HTML结果。

![架构][2]


  [1]: https://azurecomcdn.azureedge.net/mediahandler/acomblog/media/Default/blog/8f669723-2a5f-458f-be08-6fe6551d62b3.png
  [2]: https://azurecomcdn.azureedge.net/mediahandler/acomblog/media/Default/blog/40e8b655-030e-4238-8dbc-3099b4a5d0e6.png