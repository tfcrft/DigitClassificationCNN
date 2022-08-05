# DigitClassificationCNN version 1.00 Release

## 目录

1. [介绍](https://github.com/tfcrft/DigitClassificationCNN/blob/main/README.md#介绍 "介绍")
2. [导入包](https://github.com/tfcrft/DigitClassificationCNN/blob/main/README.md#导入包 "导入包")
3. [加载数据集并转换](https://github.com/tfcrft/DigitClassificationCNN/blob/main/README.md#加载数据集并转换 "加载数据集并转换")
4. [构建模型](https://github.com/tfcrft/DigitClassificationCNN/blob/main/README.md#构建模型 "构建模型")
5. [模型实例化](https://github.com/tfcrft/DigitClassificationCNN/blob/main/README.md#模型实例化 "模型实例化")
6. [设置损失函数与优化器](https://github.com/tfcrft/DigitClassificationCNN/blob/main/README.md#设置损失函数与优化器 "设置损失函数与优化器")
7. [准备模型](https://github.com/tfcrft/DigitClassificationCNN/blob/main/README.md#准备模型 "准备模型")
8. [训练模型](https://github.com/tfcrft/DigitClassificationCNN/blob/main/README.md#训练模型 "训练模型")
9. [测试模型](https://github.com/tfcrft/DigitClassificationCNN/blob/main/README.md#测试模型 "测试模型")
10. [保存模型](https://github.com/tfcrft/DigitClassificationCNN/blob/main/README.md#保存模型 "保存模型")

## 介绍

> 这个程序实现了基于[**MNIST数据集** *(http://yann.lecun.com/exdb/mnist/)*](http://yann.lecun.com/exdb/mnist/ "MNIST数据集")的黑白数字识别功能。  
> 这个程序使用[**PaddlePaddle源于产业实践的开源深度学习平台** *(https://www.paddlepaddle.org.cn/)*](https://www.paddlepaddle.org.cn/ "PaddlePaddle")打造。    
> 这个程序搭建了一个卷积神经网络，力求在性能与速度间找到平衡点。

## 导入包

```
import paddle as p
from paddle import nn
import paddle.nn.functional as F
from paddle.vision.transforms import Compose,Normalize
from paddle.metric import Accuracy
```

## 加载数据集并转换

> 这个程序采用的 ***MNIST数据集*** ，包含60,000个用于训练的手写数字示例和10,000个用于测试的手写数字示例。
