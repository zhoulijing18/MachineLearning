# 简要说明
#### 硬件设备
内存: 128G
CPU: Intel(R) Core(TM) i7-5820K CPU @ 3.30GHz

#### 运行环境
Ubuntu 16.04.2 LTS 
Python 2.7.13

#### Python Package
xgboost
lightgbm
pandas
numpy

#### 文档目录结构<br>

##### data:存放原始数据文件夹（执行前需建好）<br>
------user_action_train.txt(主办方给出的文件)<br>
------user_action_test_items.txt(主办方给出的文件)<br>
------goods_train.txt(主办方给出的文件)<br>

##### features:存放构造的特征文件夹（要执行程序之前建好）<br>
------base文件夹（要执行程序之前建好）<br>
------localtrain文件夹（要执行程序之前建好）<br>
------onlinetrain文件夹（要执行程序之前建好）<br>

##### result:存放预测结果文件夹（要执行程序之前建好）<br>
------blend（要执行程序之前建好）<br>
------local-online-xgb（要执行程序之前建好）<br>
------local-online-lgb（要执行程序之前建好）<br>
------online-online-xgb（要执行程序之前建好）<br>
------online-online-lgb（要执行程序之前建好）<br>

##### src（要执行程序之前建好）<br>
---model.py  封装相关的xgb 模型和Lgb模型<br>
---feature.py 构造模型所用的训练集和测试集（特征工程）<br>
---frame.py 封装相关的训练 预测 cv的结构<br>
---main.py 执行函数 ，执行该文件 得到预测结果。<br>

##### imp存放特征重要性文件（要执行程序之前建好）<br>


特征类别	特征名	特征说明	训练说明
基本特征	
u_id	用户唯一标识
spu_id	商品唯一标识
brand_id	商品所属的品牌标识
cat_id	商品所属的品类标识

人的特征	
u_buy_num	购买次数
u_click_num	点击次数
u_buy_date	购买天数
u_click_date	点击天数
u_num_ratio	购买点击次数比，购买次数/点击次数
u_date_ratio	购买点击天数比，购买天数/点击天数
u_buy_freq	购买频率，购买次数/90天
u_click_freq	点击频率，购买次数/90天

商品的特征	
spu_buy_num	购买次数
spu_click_num	点击次数
spu_buy_date	购买天数
spu_click_date	点击天数
spu_num_ratio	购买点击次数比，购买次数/点击次数
spu_date_ratio	购买点击天数比，购买天数/点击天数
spu_buy_freq	购买频率，购买次数/90天
spu_click_freq	点击频率，购买次数/90天

品牌的特征	
brand_buy_num	购买次数
brand_click_num	点击次数
brand_buy_date	购买天数
brand_click_date	点击天数
brand_num_ratio	购买点击次数比，购买次数/点击次数
brand_date_ratio	购买点击天数比，购买天数/点击天数
brand_buy_freq	购买频率，购买次数/90天
brand_click_freq	点击频率，购买次数/90天
品类的特征	
cat_buy_num	购买次数
cat_click_num	点击次数
cat_buy_date	购买天数
cat_click_date	点击天数
cat_num_ratio	购买点击次数比，购买次数/点击次数
cat_date_ratio	购买点击天数比，购买天数/点击天数
cat_buy_freq	购买频率，购买次数/90天
cat_click_freq	点击频率，购买次数/90天

