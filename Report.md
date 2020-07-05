[//]: # (Image References)

[image1]: images/sarsa_q-learning.JPG "sarsa q learning"
[image2]: images/plot_of_rewards_per_episode.jpg "plot of rewards per episode"

## Deep Reinforcement Learning Navigation Project Submission Report

### Overview

In this project you will train an agent to navigate (and collect bananas!) in a large, square world.

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. Four discrete actions are available, corresponding to:

0 - move forward.
1 - move backward.
2 - turn left.
3 - turn right.
The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

### Learning Algorithm

#### Deep Q-Networks (DQN):

![sarsa q learning][image1]
Also found here:
[click here](https://github.com/udacity/deep-reinforcement-learning/blob/master/cheatsheet/cheatsheet.pdf)

Paper on DQN:
[click here](https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf)

#### Hyperparameters used:

n_episodes (int): maximum number of training episodes = 2000
max_t (int): maximum number of timesteps per episode = 1000
eps_start (float): starting value of epsilon, for epsilon-greedy action selection = 1.0
eps_end (float): minimum value of epsilon = 0.01
eps_decay (float): multiplicative factor (per episode) for decreasing epsilon 0.99

### Plot of Rewards

![plot of rewards per episode][image2]

### Ideas for Future Work

#### 1. Amend the various hyperparameters
Amend the various hyperparameters and network architecture to see if you can get your agent to solve the environment faster.
You may like to implement some improvements such as prioritized experience replay, Double DQN, or Dueling DQN!

#### 1.1 Automate hyperparameter variations
You could use for example a genetic algorithm to find out what hyperparameters result in desired improvements.

#### 2. Learning from Pixels with a CNN
To solve this environment using the pixels to learn, you will need to design a convolutional neural network as the DQN architecture. For inspiration about how to set up this architecture, please refer to the DQN paper.
