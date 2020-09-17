# 集成学习 基础与算法

## 1. 结构

![image-20200901164745791](.\assets\00_1)



## 2. 章节简介

### 1. 绪论

- 基础知识&算法
- 1.5 应用：前深度学习时代的常用模型

### 2. Boosting

#### 2.1 起源

由**提出本质问题**出发：弱学习能力和强学习能力等价吗？

![image-20200901171839364](.\assets\00_2)

#### 2.2 AdaBoost

- 算法推导

- 理论探讨——为什么不容易over-fit 

  - **Margin Theory**

  - 统计视角——广义加性模型最小化对数损失函数

![image-20200901221435741](.\assets\00_3)

### 3. Bagging

#### 3.1 2种集成范式

> 强假设”分类器独立“时，可推导泛化误差上界。 

![image-20200902100504420](.\assets\00_4)

#### 3.2 Bagging

![image-20200902100847568](.\assets\00_5)

分类器：

- 敏感：e.g. 决策树
- 不敏感：e.g. 线性分类器

#### 3.3 随机树集成

- 随机森林：bagging+决策树的**升级版**——随机选择特征
- 随机化谱：决策树构造过程中产生随机节点的研究
- **Isolation Forest**



### 4. 结合方法

> boosting, bagging不过为套路，现在进入内功阶段学习。

#### 4.1 结合的益处

分3方面解释

![image-20200902102400084](.\assets\00_6)

#### 4.2 边界分析

重点关注*4.2节投票法*的理论分析

### 5. 多样性

集成学习领域的*圣杯问题*：

![image-20200902103048718](.\assets\00_7)

- 基分类器精确度不能过差，且最好犯不同的错误。
- Tradeoff：基分类器精确度越高——多样性却越低。

#### 5.2 误差分解

1. 

![image-20200902114736006](.\assets\00_8)

> 回归问题上推导得来。

👆意味着——基学习器既要error小（accuracy），又要分歧大（diversity）

2. 

![image-20200902120540805](.\assets\00_9)

——covariance 强调了**diversity**的重要性。

#### 5.3/4 多样性度量

- 统计量角度
- 信息论角度

#### 5.5 多样性增强

**如何引入随机性**

1. 数据样本
2. 输入特征
3. 学习参数
4. 输出表示



### 6. 集成修剪

#### 6.1 what&why

> 求快且省

![image-20200902122522581](.\assets\00_10)

- 串行❎ 并行✅

- 多比全好 many could be better than all （Zhou. 证明）

#### 6.2 how-方法介绍

1. 排序
2. 聚类
3. 优化



### 7. 聚类集成

![image-20200902123238294](.\assets\00_11)

![image-20200902123309605](.\assets\00_12)

### 8. 集成学习与其他范式的交叉
