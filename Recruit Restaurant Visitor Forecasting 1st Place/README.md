## Recruit Restaurant Visitor Forecasting
## 赛题
本次赛题要求选手通过一定的信息预测商店在2017.4.23~2017.5.31之间的顾客数量。
## 特征工程
该方案在构造特征时，采用了滑动窗口策略，窗口长度为39天，滑动步长为一周。下面简单介绍一下构造特征时用到的几个函数。