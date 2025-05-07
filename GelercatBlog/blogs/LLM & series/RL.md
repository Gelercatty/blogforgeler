---
title: 强化学习
date: 2025/4/30
tags:
 - AI
 - 强化学习
# categories:
#  - category2
---

# 强化学习

需要在训练过程中做生成的方法是On Policy的
On Policy是有反馈机制的，Off Policy是没有反馈机制的

On Policy: TRPO, PPO, GRPO
Off Policy: Q-learning, DPO, DQN

## 随机性策略
$\pi(a|s) = p(a_t = a|s_t = s)$

输入一个状态，输出一个动作的概率分布.
实际执行时在这个分布上采样一个动作

## 确定性策略
$a^*=argmax pi(a|s)$

智能体直接采取最有可能的动作

## 奖励模型训练， 近端策略优化
奖励模型通过由人类反馈标注的偏好数据来学习人类的偏好，判断模型回复的有用性及保证内容的安全性

奖励模型模拟了人类的偏好信息，能够不断的为模型的训练提供给奖励信号。

