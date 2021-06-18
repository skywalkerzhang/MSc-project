also, 通过对去年比赛结果的分析 —— PR分类很差，并且用2导联分类PR的相关文献很少——因此我考虑着重优化模型在PR部分的识别效果。

paced rhythm -- 介绍

s -- 做了啥



！看了一下PR的AUROC值都还蛮高的，比较低的是AUPRC和F1，是不是这意味的很多的负例被划分为了正例。所以问题更应该考虑的是如何尽量少的制造FP？

介绍 -- 提一下 PR分类很差

文献综述 -- 针对PR类，学者做了啥

According to the results of last year's competition [1], the classification result of pacing rhythm is very poor-among 41 participating teams, the highest score of F1 measure is 0.333, and the lowest score is 0. Among them, 24 teams got 0 points.

PR介绍：

Under normal circumstances, the sinus node conduction system of the heart can automatically generate cardiac electrical impulses and transmitted them to the myocardial tissue and dominate the beating of the heart. When the function of the sinus node is impaired, or certain parts of the transmission system are blocked, the sinus node of the heart cannot emit impulses, or the impulses cannot be transmitted down (or transmitted down completely) so that the heart beats extremely slowly or even stops. In order to maintain human life activities, artificial pacemakers need to be installed. Assuming that the patient's ventricular rate is lower than the minimum frequency set by the pacemaker, the pacemaker will release pacing spikes, and people can use this spike to determine whether the patient has a pacing rhythm problem.

文献综述：

Not many papers on pacing rhythm classification, but pacing rhythm can be classified by borrowing from spike detection of EEG signals. In 2003, Acır and Güzeliş used SVM model to detect spike of EEG signal[2]. They first used the pre-classifier(Autoregressive model and  Gaussian function) to divide the signal into spikes and spike-like non-spikes and trivial non-spikes. Then, they used SVM to classify spikes and spike-like non-spikes again. They applied the data to the 19-channel EEG records of 7 epilepsy patients and obtained a sensitivity of 90.3%, a selectivity of 88.1%, and a false detection rate of 9.5%. In 2013, Liu et al. proposed a new two-stage method to detect the epileptic spike[3]. They applied the k-point nonlinear energy operator (k-NEO) on the raw signals to detect all possible spike candidates in the first stage. Then, they used AdaBoost to detect spike. In the results of the two classifications, their accuracy on the training set is 100%, and the accuracy on the test set is 93.9%. In 2020, Thanh et al. proposed the simultaneous multilinear low-rank approximation of tensors (SMLRAT) algorithm[4]. They believe that single-channel EEG signals generated from different electrodes can be combined into multi-channel EEG signals. Since a certain area of the brain causes epilepsy, electrodes associated with different locations may simultaneously pick up the resulting epilepsy biomarkers. The article has two contributions: one is generalizing SLRAM from matrices to tensors. The other is applying tensor decomposition to spike detection. The results show that the accuracy of their spike detection for epilepsy has improved. 





[1][evaluation-2020/Results at master · physionetchallenges/evaluation-2020 (github.com)](https://github.com/physionetchallenges/evaluation-2020/tree/master/Results)

[2]Automatic spike detection in EEG by a two-stage procedure based on support vector machines

[3]**Model-Based Spike Detection of Epileptic EEG Data** 

[4]Multi-channel EEG epileptic spike detection by a new method of tensor decomposition