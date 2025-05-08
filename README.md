# promotion-optimizer-drl

## Overview
This project implements and compares two reinforcement learning algorithms—Deep Q-Network (DQN) and Policy Gradient using REINFORCE—to solve the problem of personalized promotional strategy optimization in a retail environment.

## Problem Statement
How can reinforcement learning be used to dynamically assign personalized promotions to customers in a way that maximizes overall business value across sales, margin, and customer retention—while adhering to promotion eligibility rules and budget constraints?

## Proposed Solution
We developed a Reinforcement Learning (RL)-based Promotion Recommendation System to personalize offers for customers based on their profiles and historical behavior. The system aims to maximize long-term rewards like sales uplift, profit, and customer retention.

## Problem as MDP
State: Customer features (e.g., age, income, loyalty, churn score)                 
Action: Select one of 10 promotions (PR100–PR109) based on segment eligibility               
Reward: Combines sales (log1p(qty × price)), profit, engagement, and retention

Algorithms Used
DQN: Value-based Deep Q-Network with experience replay & target networks               
PPO: Policy-gradient approach using softmax with action masking

Action Masking
Ensures only eligible promotions are recommended per customer segment

Evaluation
Metrics: Average reward, engagement rate, sales & margin impact             
DQN showed faster convergence and better stability than PPO
