# 转化率预估技术

## 1. Papers

## MPC Problem

MPC: multi conversion per click 每次点击多次转化

1. **Handling many conversions per click in modeling delayed feedback**（AdKDD，2021，[Handling many conversions per click in modeling delayed feedback](http://papers.adkdd.org/2021/papers/adkdd21-badanidivuru-handling.pdf)）：这篇论文介绍了如何处理每次点击可能产生多次转化的问题。作者提出了一种基于三个核心思想的无偏估计模型。第一个思想是将标签分解为不同延迟桶的标签之和，每个桶只对成熟的标签进行训练；第二个思想是使用温度编码来提高精度并降低推理成本；第三个思想是使用辅助信息来增加模型的稳定性并处理分布的漂移⁵。

2. **Modeling labels for conversion value prediction**（AdKDD，2021，[Modeling labels for conversion value prediction](http://papers.adkdd.org/2021/papers/adkdd21-badanidiyuru-modeling.pdf)）：这篇论文探讨了如何更好地建模标签并从特征中提取尽可能多的信息。作者研究了由广告商报告的标签引起的三个主要问题，并提出了新的技术来解决它们。第一个问题是标签的规模可能会影响模型的容量如何分配给不同的广告商；第二个问题是异常值标签如何影响过拟合；最后，作者还展示了标签的分布包含了重要的信息，我们应该训练我们的模型使用它们，而不仅仅依赖于均值¹。

## Delay Feedback Problem

1. **DFM**（KDD，2014，[Modeling Delayed Feedback in Display Advertising](https://dl.acm.org/doi/abs/10.1145/2623330.2623634)）：这篇论文介绍了一个模型，该模型在性能展示广告中捕获转化延迟。该模型有助于确定是否应将尚未转化的用户视为负样本，或者应从训练集中丢弃。

2. **NoDef**（无会议信息，[A Nonparametric Delayed Feedback Model for Conversion Rate Prediction](https://arxiv.org/pdf/1802.00255.pdf)）：这篇论文提出了一个非参数延迟反馈模型，用于转化率（CVR）预测，该模型表示时间延迟的分布，而无需假设参数分布。

3. **FNW** 和 **FNC**（2019年，[Addressing delayed feedback for continuous training with neural networks in CTR prediction](https://arxiv.org/pdf/1907.06558.pdf)）：这些论文解决了在展示广告的转化率预测中连续训练的延迟反馈挑战。他们提出了处理假负面的不同机制。

4. **ES-DFM**（AAAI，2019，[Capturing delayed feedback in conversion rate prediction via elapsed-time sampling.](https://arxiv.org/pdf/2012.03245.pdf)）：这篇论文提出了过去时间采样延迟反馈模型（ES-DFM），该模型模拟了观察到的转化分布与真实转化分布之间的关系。它通过在过去时间采样分布下的重要性采样优化真实转化分布的期望。

5. **DEFUSE/Bi-DEFUSE**（WWW，2022，[Asymptotically Unbiased Estimation for Delayed Feedback Modeling via Label Correction](https://arxiv.org/pdf/2202.06472.pdf)）：这篇论文提出了一种新方法，即通过标签修正进行无偏估计的延迟反馈建模（DEFUSE），该方法旨在以更细的粒度纠正即时正面、假负面、真实负面和延迟正面样本的重要性权重。

6. **FTP**（SIGIR，2021，[Follow the Prophet: Accurate Online Conversion Rate Prediction in the Face of Delayed Feedback](https://arxiv.org/pdf/2108.06167.pdf)）：这篇论文提出通过“跟随先知”（FTP）来解决在线广告中的延迟反馈问题。关键的见解是，如果所有记录的样本的反馈都立即到来，我们就可以得到一个没有延迟反馈的模型，即“先知”。

7. **DFSN-alpha, DFSN-beta**（SIGIR，2023，[Online Conversion Rate Prediction via Neural Satellite Networksin Delayed Feedback Advertising](https://dl.acm.org/doi/pdf/10.1145/3539618.3591747)）：这篇论文提出了通过神经卫星网络进行延迟反馈建模（DFSN）进行在线CVR预测。它解决了数据新鲜度的问题，以允许自适应等待窗口。


Others:

1. **A Feedback Shift Correction in Predicting Conversion Rates under Delayed Feedback**: This paper addresses the problem of feedback shift in conversion rate prediction by using an importance weight approach typically used for covariate shift correction³¹.

2. **A Multi-Task Learning Approach for Delayed Feedback Modeling**: This paper identifies the best combination of loss functions and models that enable large-scale learning from a continuous stream of data in the presence of delayed labels⁷⁵.

3. **A Nonparametric Delayed Feedback Model for Conversion Rate Prediction**: This paper proposes a nonparametric delayed feedback model for conversion rate prediction that represents the distribution of the time delay without assuming a parametric distribution¹⁹[^20^].

4. **Addressing Delayed Feedback for Continuous Training with Neural Networks in CTR prediction**: This paper identifies the best combination of loss functions and models that enable large-scale learning from a continuous stream of data in the presence of delayed labels²⁶²⁷.

5. **An Attention-based Model for Conversion Rate Prediction with Delayed Feedback via Post-click Calibration**: This paper proposes a novel deep learning framework to tackle the challenges of data sparsity and delayed feedback in conversion rate prediction¹⁴¹⁸.

6. **Asymptotically Unbiased Estimation for Delayed Feedback Modeling via Label Correction**: This paper proposes a new method, DEFUSE, which aims to correct the importance weights of the immediate positive, the fake negative, the real negative, and the delay positive samples at finer granularity³²[^10^].

7. **Capturing Delayed Feedback in Conversion Rate Prediction via Elapsed-Time Sampling**: This paper proposes a method that models the relationship between the observed conversion distribution and the true conversion distribution¹⁴.

8. **Counterfactual Reward Modification for Streaming Recommendation with Delayed Feedback**: This paper proposes a novel and theoretically sound counterfactual approach to streaming recommendation with delayed feedback³².

9. **Delayed Feedback Model with Negative Binomial Regression for Multiple Conversions**: I couldn't find an abstract for this paper.

10. **Delayed Feedback Modeling for the Entire Space Conversion Rate Prediction**: This paper proposes a novel neural network framework ESDF to tackle the challenges of data sparsity, sample selection bias, and delayed feedback in conversion rate prediction⁴¹⁵.



## Uncertancy Callibration

[阿里妈妈展示广告预估校准技术演进之路](https://zhuanlan.zhihu.com/p/405826307) By DataFunTalk 

[huangsg uncertaity-callibration github](https://github.com/huangsg1/uncertainty-calibration) By Huangsiguang
 

## Metrics Problem
Robustness

模型方差(Variance):  模型在不同数据集上预测结果的波动性和不稳定性。方差是一种度量模型访华能力的指标，反应了模型对于训练数据变化敏感程度。比如准确率的方差。方差大说明模型出现过拟合，通过缓解模型过拟合的方法来做。



# 2 中文材料和开源项目
[转化延迟 Delayed Feedback in Streaming Learning](https://zhuanlan.zhihu.com/p/657043621) By lxsabrina 

[一文搞懂CTR建模](https://zhuanlan.zhihu.com/p/582534683) By Coreyzhong

[一文让你更懂 CTR 建模](https://zhuanlan.zhihu.com/p/582534683) By coreyzhong

[Mobius 论文研读与想法 ](https://zhizhou-yu.github.io/2020/09/12/Mobius.html) KDD, 2019

[全空间多任务模型 ESMM](https://github.com/alibaba/x-deeplearning/wiki/%E5%85%A8%E7%A9%BA%E9%97%B4%E5%A4%9A%E4%BB%BB%E5%8A%A1%E6%A8%A1%E5%9E%8B(ESMM))


https://github.com/tangxyw/RecSysPapers/blob/main/Feedback-Delay/Modeling%20Delayed%20Feedback%20in%20Display%20Advertising.pdf