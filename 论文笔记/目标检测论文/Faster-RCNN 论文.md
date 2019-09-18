<!-- update 论文笔记  faster-rcnn-->
# <div align=center> Faster-RCNN 论文阅读 </div>
## &emsp;&emsp; Faster-RCNN是典型two-stage检测法，就是将检测问题分为两个阶段，首先是生成候选区域，然后对候选区域进行分类，是先做检测，然后在做分类。不像SSD和YOLO同时进行分类和检测，loss是两者的loss相加。典型的算法就是R-CNN系列，Faster-RCNN就是基于region proposal的目标检测---Faster-RCNN。

## &emsp;&emsp; Faster-RCNN 的核心是RPN，区域生成网络。

## &emsp;&emsp; RPN生成的框可以看做是Anchors，特征可以看做一个尺度W✖️H✖️C通道的图像，对于该图像的每一个位置，考虑有9个可能的候选框,三种尺度{128,256,512}和三种比例{1:1,1:2,2:1}
