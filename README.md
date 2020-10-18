<p align="center">
  <img src="https://github.com/addy1997/RL-Algorithms/blob/master/assets/logo.jpg"/>
</p>


[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg)](LICENSE)  [![Build Status](https://ci.appveyor.com/api/projects/status/8e784doc5sye7c41?svg=true)](https://ci.appveyor.com/project/addy1997/RL-Algorithms)  [![Stars](https://img.shields.io/github/stars/addy1997/RL-Algorithms.svg?style=flat&label=Star&maxAge=86400)](STARS) [![Contributions](https://img.shields.io/github/commit-activity/m/addy1997/RL-Algorithms.svg?color=%09%2346c018)](https://github.com/addy1997/RL-Algorithms/graphs/commit-activity) [![Lines Of Code](https://tokei.rs/b1/github/addy1997/RL-Algorithms?category=code)](https://github.com/addy1997/RL-Algorithms)   [![Total alerts](https://img.shields.io/lgtm/alerts/g/addy1997/RL-Algorithms.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/addy1997/RL-Algorithms/alerts/) [![Code](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/ambv/black)  [![CodeFactor](https://www.codefactor.io/repository/github/addy1997/RL-Algorithms/badge)](https://www.codefactor.io/repository/github/addy1997/RL-Algorithms)

#### Table of Contents

* [Epsilon](#Epsilon)
* [SARSA](#SARSA)
* [Q_learning](#Q_learning)
* [Expected-SARSA](#Expected-SARSA)
* [Double-SARSA](#Double-SARSA)
* [Expected-Double-SARSA](#Expected-Double-SARSA)
* [References](#References)

## [Epsilon](#RL-Algorithms)


## [SARSA](#RL-Algorithms)

# Algorithm 
![logo](https://github.com/addy1997/RL-Algorithms/blob/master/assets/SARSA_psuedo.png)

# Theory

**SARSA** or _State-Action-Reward-State-Action_ is an algorithm based on **on-policy** **TD(0)** control method in reinforcement learning.
It follows **Generalised Policy Iteration** strategy: as the policy **π** becomes greedy with respect to the state-action value function, the state-action value function becomes more optimal. Our aim is to estimate **Qπ(s, a)** for the current policy π and all state-action (s-a) pairs.

* We learn the **state-action value** function **Q(s,a)** rather than **state-value** **V(s)**.
* Here, **qπ(s,a)** is the estimate for the current **behavior policy π** for all the state-actions pairs (s,a).
* Initialising a suitable state **s** (s should not be a terminal state).
* Choose an appropriate action **A** under the policy **epsilon-greedy or epsilon-soft**.
* Record the values of the **state S'** and the **reward R**.
* Update the function -> _Q(S, A) ← Q(S, A) + αR + γQ(S′, A′) − Q(S, A)_

* This loop runs till it encounters a terminal state where **Q(s',a')** = 0.

# SARSA update rule

![logo](https://github.com/addy1997/RL-Algorithms/blob/master/assets/sarsa2.png)

## [Q_learning](#RL-Algorithms)

**Q-learning** similar to **SARSA**, is based on **off-policy TD(0)** control method. Both the algorithms aim to estimate the **Qπ(s, a)** value for all the **state-action** pairs invlved in the task. 

# Q-learning Algorithm 

![logo](https://github.com/addy1997/RL-Algorithms/blob/master/assets/Q_learning2.png)

# Q-leaning vs SARSA
The only difference is that in **SARSA** the action **a'** to go from **current state** to the **next state** is selected by the same policy **π** (behavioral policy). Whereas in **Q-learning**, the action **a'** to go from **present state** to **next state** is selected in **greedy** manner, i.e., there are fewer chances of choosing a random action in a state. Hence, it involves more explotaiton than exploration. 

# Q-learning update rule
![logo](https://github.com/addy1997/RL-Algorithms/blob/master/assets/Q_learning1.png)


## [Expected-SARSA](#RL-Algorithms)

# Algorithm

![algorithm](https://github.com/addy1997/RL-Algorithms/blob/master/assets/expected-sarsa.png)


## [Double-SARSA](#RL-Algorithms)


## [Expected-Double-SARSA](#RL-Algorithms)



## [References](#RL-Algorithms)

* [Vanilla DQN, Double DQN, and Dueling DQN in PyTorch](https://github.com/dxyang/DQN_pytorch)
* [Deep Reinforcement Learning for Keras](https://github.com/keras-rl/keras-rl)
* [Deep Reinforcement Learning with pytorch & visdom](https://github.com/jingweiz/pytorch-rl)
* [Minimal PyTorch DQN](https://github.com/econti/minimal_dqn)
* [deep-Q-networks: Implementation of algorithms from the Q-learning family](https://github.com/cyoon1729/deep-Q-networks)
* [keras-rl2 ](https://github.com/wau/keras-rl2)
* [RL-Adventure](https://github.com/higgsfield/RL-Adventure)
