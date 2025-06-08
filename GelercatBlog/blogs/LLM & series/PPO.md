# PPO
近端策略优化，Proximal Policy Optimization PPO Openai 2017 提出的 强化学习算法


## 涉及的四个模型

- 策略模型（Policy Model），用于生成模型回复
- 奖励模型（Reward Model），输出奖励分数来评估回复好坏
- 评论模型（Critic Model），预测回复的好坏，可以在训练过程中实时调整模型，选择对未来积累收益最大的行为
- 参考模型（Reference Model），一个SFT模型的备份，帮助模型不会出现过于极端的变化


## PPO的实施流程
- 环境采样： Policy Model 基于给定输入生成一系列的回复，Reward Model 对这些回复进行打分获得奖励
- 优势估计： Critic Model 预测生成回复的未来积累奖励，