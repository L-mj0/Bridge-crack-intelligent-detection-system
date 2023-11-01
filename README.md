# 桥梁裂缝智能检测系统

1.流程图

![](images/1.png)

**Yolo v5部分流程：**

利用GitHub获得yolo v5开源代码与预训练权重，通过Anaconda装配pytorth环境，利用已有labelimg对已有数据集（如需预处理则使用opencv进行批量化预处理）进行分类、切分与标注。

针对标注对源代码进行改动，同时调整学习率、轮数等参数。

通过多组尝试不同标签与参数、不同权重的组合，筛选置信度峰值的权重，并进行对比试验，验证更多样本情况下的识别成功率与稳定性。

**Yolo v7部分流程：**

与yolo v5大致相同，需注意，yolo v7中需求软件包与v5有所区别，pytorth可沿用v5版本，需通过pip加入requests中缺失的包。如安装不成功，亦可通过pypi下载至本地通过终端进行安装，实验中同v5一致，需进行多轮组合，调整权重、参数等，筛选出置信度峰值权重，最终进行对比试验。需与v5结果进行对比，比较出更适合与裂缝识别的算法与权重参数组合。为后期的硬件移植和可视化实现提供基础。

### 界面

![2](images/2.jpg)



![3](images/3.png)# Bridge-crack-intelligent-detection-system
