# 大数据

a hub for task: https://tianchi.aliyun.com/dataset/140667

Team member：

- 葛涛
- 刘祥盛
- 张庆伟

## 数据处理

处理思路（针对训练集）：

1. 异常样本处理：
   
1）value值过大或过小的样本，删除；

2）NH1543、NH1544、NH1545、NH1546、NH1573、NH1574这6个样本有完全相同的重复行，删除；

2. 异常特征处理：

1）时间特征，删除；

2）方差为0（过小）的特征，删除；

3）特征间相关性（线性化）过高的特征，只保留一条以显示信息，其余删除；

4）数据缺失过多的特征（为0或空），删除；

5）特征值唯一的数据，删除；（未完成）

6）不符合正态分布的特征，删除；（未完成）

3. 缺失值处理：

对于缺失值较少的特征，使用均值填充；

4. 其他：

将文本数据转化为数值数据；

数据标准化；

处理后的数据保存为train.xlsx文件。