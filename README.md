# RL_Power_Grid 

This repository contains implementations of **Deep Q-Network (DQN)** and **Proximal Policy Optimization (PPO)** models applied to a custom environment for power grid stabilization using the **Grid2Op** simulation framework. The objective of this project is to assess and enhance the performance of reinforcement learning agents in maintaining grid stability and maximizing power flow under **N-1 security constraints**. The project explores different configurations, including **reward shaping**, **action enhancements**, and **scheduling observation**, to improve agent performance and training stability.

## Project Overview

The notebook evaluates the following models:

### DQN Models:
- **DQN Base**: Standard Deep Q-Network without modifications.
- **DQN + Reward Shaping**: Adds reward shaping to guide the agent's learning process more effectively.
- **Dueling DQN + Reward Shaping**: Combines the Dueling Architecture and reward shaping, where the Dueling Architecture separates the state value and advantage functions to improve stability.

### PPO Models:
- **PPO Base**: Standard PPO algorithm without modifications.
- **PPO + Action**: Adds enhanced actions to the base PPO model for improved decision-making capabilities.
- **PPO + Action + Scheduling Observation**: Combines enhanced actions and scheduling observation to provide the agent with a more informed view, allowing it to anticipate and respond to power grid changes effectively.

Each model is evaluated based on its ability to maximize cumulative rewards and maintain stability under grid perturbations.

## Evaluation Metrics:
- **Rewards**: Total rewards accumulated by the agent during evaluation episodes, indicating effective power flow management.
- **Episode Length**: The number of steps per episode, which reflects the agent’s efficiency in grid stabilization.

## Requirements
To run the notebook, the following Python libraries are required:
- **stable-baselines3**: Reinforcement learning library that includes PPO and DQN implementations.
- **gym**: Toolkit for developing and comparing reinforcement learning algorithms.
- **numpy**: For numerical operations.
- **matplotlib**: For visualizing evaluation results.
- **grid2op**: Simulator specifically for testing power grid operations.

## Visualization and Analysis
The notebook also provides code for:
- **Plotting Results**: Compare the rewards and episode lengths for each DQN and PPO model using line plots.
- **Statistics**: Display key metrics such as the mean and standard deviation of rewards and episode lengths.

These visualizations help to highlight performance differences, offering insights into which configurations yield the best results for grid stability.

## Results
The key findings from running the evaluation are:
- **Reward Shaping**: Guides the agent toward better performance by providing intermediate rewards.
- **Dueling DQN Architecture**: Improves stability by separating the value and advantage functions, reducing variance in rewards.
- **PPO Dual Network Architecture**: Stabilizes training by separating policy and value heads, especially effective when combined with reward shaping.
