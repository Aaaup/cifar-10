# cifar-10
### 项目说明：<br>
本项目旨在使用深度学习对CIFAR-10数据集进行图像分类。
CIFAR-10是一个广泛使用的图像数据集，包含10个类别的60,000张32x32彩色图像。
项目中使用了卷积神经网络(CNN)和注意力机制来提高分类准确性。

### 代码结构：<br>
AttentionModule 类：定义了一个简单的注意力机制模块，用于增强模型对图像特征的学习能力。
CustomNet 类：自定义的神经网络结构，集成了注意力模块，用于图像分类任务。
l2_regularization 函数：计算模型参数的L2正则化项，用于防止过拟合。
get_net 函数：获取用于训练的神经网络模型。
train 函数：执行模型训练的函数，包括正则化和学习率调度。
数据预处理和加载部分：使用 torchvision 和 torch.utils.data 对CIFAR-10数据集进行预处理、加载和批处理。

## 运行方式：<br>
### 安装依赖： <br>
确保安装了所需的Python库，包括torch, torchvision, d2l, py7zr, pandas。
可以通过运行以下命令安装：<br>
!pip install d2l!pip install py7zr
### 准备数据：<br>
将CIFAR-10数据集的.7z文件放入/kaggle/input/cifar-10/目录下，并将trainLabels.csv复制到/kaggle/working/目录下。
### 数据整理：<br>
运行脚本将自动解压数据集，并按照训练集、验证集和测试集进行组织。
### 模型训练：<br>
设置好超参数后，运行训练函数 train 开始训练模型。
### 模型评估：<br>
训练完成后，使用测试集对模型进行评估。
### 生成提交文件：<br>
根据模型预测结果生成提交文件 submission.csv。
### 超参数说明：<br>
batch_size：每个批次的样本数量。<br>
valid_ratio：从训练集中划分用于验证的比例。<br>
num_epochs：训练的轮数。<br>
lr：学习率。<br>
wd：权重衰减（L2正则化系数）。<br>
lr_period 和 lr_decay：学习率衰减周期和衰减率。


