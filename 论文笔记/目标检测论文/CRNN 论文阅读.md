# CRNN 论文阅读
[论文地址下载](https://arxiv.org/pdf/1507.05717v1.pdf)
## &emsp;&emsp; 论文的思路和方法
### &emsp;&emsp;&emsp;  1. 问题范围:字符识别
### &emsp;&emsp;&emsp;  2. CNN层:使用标准的CNN提取图像特征,利用Map-to-Sequence (按照顺序映射)表示特征向量;
### &emsp;&emsp;&emsp;  3. RNN层;使用双向LSTM识别特征向量,得到每列特征的概率分布;
### &emsp;&emsp;&emsp;  4. Transcription层;利用CTC和前向算法求解最优的label序列
## &emsp;&emsp; 两点和创新点
### &emsp;&emsp;&emsp;  1. 端到端可训练(将CNN和RNN联合训练)
### &emsp;&emsp;&emsp;  2. 任意长度的输入(图像宽度任意,单词长度任意)
### &emsp;&emsp;&emsp;  3. 训练集无需有字符的标定
### &emsp;&emsp;&emsp;  4. 带字典和不带字典的库(样本)都可以使用
### &emsp;&emsp;&emsp;  5. 性能好,而且模型小(参数少)
