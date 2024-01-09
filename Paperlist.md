# 广告召回技术
## 1. Papers



## 2.中文材料
[Mobius 论文研读与想法 ](https://zhizhou-yu.github.io/2020/09/12/Mobius.html) KDD, 2019







# 广告转化率预估技术
## 1. Papers

[Handling many conversions per click  in modeling delayed feeback](http://papers.adkdd.org/2021/papers/adkdd21-badanidivuru-handling.pdf) By Ashwinkumar Badanidiyuru et al. Adkdd, 2021

[Modeling labels for conversion value prediction](http://papers.adkdd.org/2021/papers/adkdd21-badanidiyuru-modeling.pdf) By Ashwinkumar Badanidiyuru et al. Adkdd, 2021 


## 2. Application(应用)

## 3. Metrics（评价方法）
Robustness

模型方差(Variance):  模型在不同数据集上预测结果的波动性和不稳定性。方差是一种度量模型访华能力的指标，反应了模型对于训练数据变化敏感程度。比如准确率的方差。方差大说明模型出现过拟合，通过缓解模型过拟合的方法来做。

## 4. DataSets and Benchmarking（公开数据集）

## 5. 中文材料

[WWW 2022 | 搜索广告CVR延迟反馈建模DEFUSE](https://zhuanlan.zhihu.com/p/506476146)书浅、澍元、石士

[转化延迟 Delayed Feedback in Streaming Learning](https://zhuanlan.zhihu.com/p/657043621) By lxsabrina 

[一文搞懂CTR建模](https://zhuanlan.zhihu.com/p/582534683) By Coreyzhong

[一文让你更懂 CTR 建模](https://zhuanlan.zhihu.com/p/582534683) By coreyzhong



## 6. 开源项目

[全空间多任务模型 ESMM](https://github.com/alibaba/x-deeplearning/wiki/%E5%85%A8%E7%A9%BA%E9%97%B4%E5%A4%9A%E4%BB%BB%E5%8A%A1%E6%A8%A1%E5%9E%8B(ESMM))


# Uncertainty Calibration(预估校准技术)

## 1. Papers

## 2. Application(应用)

## 3. Metrics（评价方法）

## 4. DataSets and Benchmarking（公开数据集）

## 5. 中文材料
[阿里妈妈展示广告预估校准技术演进之路](https://zhuanlan.zhihu.com/p/405826307) By DataFunTalk 

[huangsg uncertaity-callibration github](https://github.com/huangsg1/uncertainty-calibration) By Huangsiguang
 


# Delayed Feedback Problem in online advertising

## 1.Papers

DFM  [Modeling Delayed Feedback in Display Advertising](https://dl.acm.org/doi/abs/10.1145/2623330.2623634),By Criteo, KDD, 2014

NoDef [A Nonparametric Delayed Feedback Model for Conversion Rate Prediction](https://arxiv.org/pdf/1802.00255.pdf) By Yuya Yoshikawa1, 

FNW:A model training with a duplication mechanism using the fake negative weighted loss.  [Addressing delayed feedback for continuous training with neural networks in CTR prediction](https://arxiv.org/pdf/1907.06558.pdf) ,2019

FNC:A model training with a duplication mechanism with the fake negative calibration. [Addressing delayed feedback for continuous training with neural networks in CTR prediction](https://arxiv.org/pdf/1907.06558.pdf) ,2019

ES-DFM: A model training with a duplication mechanism using the ES-DFM loss. [Capturing delayed feedback in conversion rate prediction via elapsed-time sampling.](https://arxiv.org/pdf/2012.03245.pdf) AAAI, 2019

DEFUSE/Bi-DEFUSE: A model training with a duplication mechanism using the DEFUSE loss. [Asymptotically Unbiased Estimation for Delayed Feedback Modeling via Label Correction](https://arxiv.org/pdf/2202.06472.pdf) By YuChen, WWW, 2022

FTP: A model training with a multi-task learning and aggregation mechanism. [Follow the Prophet: Accurate Online Conversion Rate Prediction in the Face of Delayed Feedback](https://arxiv.org/pdf/2108.06167.pdf) ,SIGIR, 2021

DFSN-alpha, DFSN-beta  [Online Conversion Rate Prediction via Neural Satellite Networksin Delayed Feedback Advertising](https://dl.acm.org/doi/pdf/10.1145/3539618.3591747) By Qiming Liu, SIGIR, 2023


## 2.中文材料

https://github.com/tangxyw/RecSysPapers/blob/main/Feedback-Delay/Modeling%20Delayed%20Feedback%20in%20Display%20Advertising.pdf


# AutoBidding 自动出价技术

## 1. Papers
[AutoBidding with Constraints](https://link.springer.com/chapter/10.1007/978-3-030-35389-6_2)   By Gagan Aggarwal et al. 2019

 - Abstract：


## 2. Application(应用)

## 3. Metrics（评价方法）

## 4. DataSets and Benchmarking（公开数据集）

## 5. 中文材料

# Common Hard Questions
## 1. 模型训练方差大


# Auction Design

[KDD2021 | USCB:展示广告约束出价问题的通用解决方案](https://mp.weixin.qq.com/s?__biz=Mzg5NTk4MDMwMA==&mid=2247490332&idx=2&sn=b726773d679338f867b56c80aed5a51a&chksm=c0095d7ff77ed469875aae7b1fe0dcc8e6c0be24c096579bad94675464dbcdd31d37c7821198&scene=21#wechat_redirect)