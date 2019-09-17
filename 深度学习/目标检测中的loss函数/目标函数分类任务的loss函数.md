# 目标检测分类任务的loss函数

## &emsp;&emsp; 分类问题的目标变量是离散的，神经网络模型的效果及优化的目标就是通过自定义损失函数来定义的。

## &emsp;&emsp;分类问题常用的损失函数为交叉熵(Cross Entropy Loss)。

## &emsp;&emsp;交叉熵描述了两个概率分布之间的距离，当交叉熵越小说明两者之间越接近。尽管交叉熵刻画的两个概率分布之间的距离,但是神经网络的输出却不一定就是概率分布，为此我们常常使用Softmax回归任务将神经网络前向传播得到的结果变成概率分布。
  
## &emsp;&emsp;Softmax常用于多分类的问题，它将多个神经元的输出归一化到(0,1)之间，因此Softmax的输出可以看成是概率，从而进行多分类。
  
## &emsp; &emsp;假设我们有一个包含K个元素的数组V,i表示V中的第i个元素，那么这个i元素的Softmax就是 
<!--<div align=center><img width="150" height="150" src="http://chart.googleapis.com/chart?cht=tx&chl= ![](http://chart.googleapis.com/chart?cht=tx&chl= $S_i = \frac{e^i }{sum^{j==k}_{j =1}{e^j}})"/></div>-->
<!--![](https://chart.apis.google.com/chart?cht=tx&chf=bg,s,FFFF00&chl= $S_i = \frac{e^i }{sum^{j==k}_{j =1}{e^j}}$)-->
$S_i = \frac{e^i }{sum^{j==k}_{j =1}{e^j}}$

![](http://chart.googleapis.com/chart?cht=tx&chl=$S_i = \frac{e^i }{sum^{j==k}_{j =1}{e^j}}$)

<!--
<center><font face="黑体" size=7> $S_i = \frac{e^i }{sum^{j==k}_{j =1}{e^j}}$</font> </center>-->



