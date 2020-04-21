# 客户流失预测Sparkify 项目

## 运行所需

### 开发环境

程序正常运行需要如下软件包：

- `pyspark`：Python运行Spark所需要的依赖库
- `seaborn`：对数据分析并绘制可视化图形
- `matplotlib`：Python基础的绘制可视化图形工具
- `pandas`：Python中常见的数据分析软件
- `numpy`：数据处理常用的工具，善于矩阵运算



### 数据集

- `mini_sparkify_event_data.json`：在线音乐软件使用过程的数据集。



## 项目简介

### 项目背景

此项目是优达数据挖掘纳米学位的毕业新项目，实践用的数据集采用某在线音乐项目的用户使用过程中的数据，诸如用户操作，如听歌、点赞、添加朋友、加入播放列表等行为日志，完整的数据集为12GB，本项目分析完整数据集的一部分，使用Spark集群进行分析，进而迁移到大数据集上。本项目的目的是根据用户以往的行为数据利用机器学习算法预测可能出现的客户流失。



### 数据结构

数据共有286500条数据，包含如下特征：

- userId:用户ID
- sessionId:会话ID

- artist：歌手

- auth:登录状态，可能的取值为Logged Out,Cancelled,Guest,Logged In

- gender:性别，可能的取值为F和M

- level:会员等级，可能的取值为free和paid

- page:请求页面，可能的取值为

  - Cancel：取消
  - Submit Downgrade：提交降级
  - Thumbs Down：鄙夷
  - Home：查看主页
  - Roll Advert：滚动广告
  - Logout：退出
  - Save Settings：保存设置
  - Cancellation Confirmation：确定取消
  - About：关于
  - Submit Registration：提交注册
  - Settings：设置
  - Login：登录
  - Register：注册
  - Add to Playlist：添加至播放列表
  - Add Friend：添加好友
  - NextSong：下一曲
  - Thumbs Up：点赞
  - Help：求助
  - Upgrade：查看升级

- registration:注册时间

- song:歌名

- status:可能取值为202，400，307

- ts:时间

- userAgent:用户使用设备


## 数据分析

### 概述

- 将数据加载到Spark上，并使用Spark DataFrame对数据进行分析
- 分析数据存在的问题，并进行数据清洗
- 对清洗后的数据进行探索性分析
- 将数据划分为训练集、验证集、测试集，利用机器学习算法训练机器学习算法训练并在训练集上评估效果



### 数据标签

使用Cancellation Confirmation定义用户流失。



### 数据探索分析思路

提取与客户流失有较强相关的特征绘制图表观察



### 特征工程

根据图表分析结果构建机器学习的特征。



### 评估指标

利用F1 Score实现集精度和召回率平衡的指标。



### 建模

构建二分类的机器学习算法利用训练集训练算法，并在验证集上进行交叉验证，选择出表现最好的参数组合，并在测试集上纪念性验证。



## 项目文件

- [包含源代码的和处理过程的文件](Sparkify-zh.ipynb)

- [项目报告日志](Sparkify_Report.md   )



