# MH-DRL
    Multi-agent Deep Reinforcement Learning for Hyperspectral Band Selection with Hybrid Teacher Guide Knowledge-Based Systems
    Jie Feng *, Qiyang Gao , Ronghua Shang , Xianghai Cao , Gaiqin Bai , Xiangrong Zhang , Licheng Jiao

## A B S T R A C T
由于高光谱图像(HSIs)中存在噪声和高度冗余的波段，波段选择是下游分类任务的关键预处理。最近，深度强化学习 (DRL) 已成为 HSI 波段选择的新趋势。现有的基于drl的方法通常采用单智能体，由于动作空间过多，容易陷入局部最优。多智能体方法提供了一种可行的解决方案，但通常需要太多的计算。为了解决这些问题，提出了一种新的混合教师引导(MH-DRL)多智能体DRL方法，用于HSIS的波段选择。在MH-DRL中，对应于光谱波段的每个代理决定是否选择该波段。此外，构建了一个表示评估网络（PE-Net），通过在没有任何微调的情况下评估候选波段子集来设计奖励，并通过提取 HSI 的空间光谱特征来表示状态。然后，将三种经验丰富的波段选择模型作为教师，设计参与DRL波段探索，通过积累来自不同教师模型的外部知识来提高学习的有效性和效率。最后，设计了深度Q学习算法来更新智能体，并从连续探索中提高自学习能力。在三个广泛使用的HSI数据上的实验结果表明，该方法的性能优于一些先进的HSI波段选择算法。

## 提出的MH-DRL方法的框架。红色波段表示所选波段，灰色波段表示未选择波段。
![image](https://github.com/jiefeng0109/MH-DRL/assets/26159369/c97aaa5f-deac-4e49-a801-8d5a8ca2ff1c)

## 设计的深度 Q 网络的框架。
![image](https://github.com/jiefeng0109/MH-DRL/assets/26159369/a7d7812e-7630-4dd1-8280-c095cfd2fd7f)


