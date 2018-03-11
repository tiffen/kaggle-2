## Recruit Restaurant Visitor Forecasting
## 赛题
本次赛题要求选手通过一定的信息预测饭店在2017.4.23~2017.5.31之间的顾客数量。
## 特征工程
该方案在构造特征时，采用了滑动窗口策略，窗口长度为39天，滑动步长为一周。下面简单介绍一下构造特征时用到的几个函数。  
* get_store_visitor_feat</br>
统计每个饭店一段时间范围内顾客数量的最小值、最大值、平均值、中位数、出现了多少次、标准差和偏度。</br>
* get_store_exp_visitor_feat</br>
计算每个饭店顾客数量的指数加权平均值。</br>
* get_store_week_feat</br>
统计每个饭店在每个周几顾客数量的最小值、最大值、平均值、中位数、出现了多少次、标准差和偏度。</br>
* get_store_week_diff_feat</br>
计算每个饭店当天与前一天顾客数之差的平均值、标准差、最大值和最小值。</br>
* get_store_all_week_feat</br>
计算每个饭店每个周几顾客数量的平均值、中位数、最大值和出现了多少次。</br>
* get_store_week_exp_feat</br>
计算每个饭店每个周几顾客数量的指数加权平均值。</br>
* get_store_holiday_feat</br>
统计两种节假日下，每个饭店顾客数量的最小值、平均值、中位数、最大值、出现了多少次、标准差以及偏度。</br>
* get_genre_visitor_feat</br>
统计每种类型饭店一段时间范围内顾客数量的最大值、最小值、平均值、中位数、出现了多少次、标准差以及偏度。</br>
* get_genre_exp_visitor_feat</br>
计算每种类型饭店顾客数量的指数加权平均值。</br>
* get_genre_week_feat</br>
统计每种类型饭店每个周几顾客数量的最小值、平均值、中位数、出现了多少次、最大值、标准差以及偏度。</br>
* get_genre_week_exp_feat</br>
计算每个类型饭店每个周几顾客数量的指数加权平均值。</br>
* get_first_last_time</br>
统计每个商店第一次和最后一次出现距离滑动窗口的天数。</br>
* get_reserve_feat</br>
提取一些与预定信息相关的特征。
## 模型
* lightgbm
## 语言
* python3
## 运行
将原始数据文件放入../data/目录下，运行python script.py即可。
