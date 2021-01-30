# Report

The goal of this project is to train an agent to solve the Unity Banana Collector environment. The environment contains blue and yellow bananas. The task is to teach the agent to collect the yellow bananas and avoid the blue ones.

## Learning algorithm

The learning algorithm used for this solution is Q-learning implemented with deep learning, i.e. Deep Q-learning.

Q-learning learns the action-value function, it determines the value of taking an action at a certain state by assigning a scalar for every action at every state. It also balances exploration (trying new previously untried or rarely tried actions at certain states) and exploitation (using the action that would provide the best reward at the given state).

Deep Q-learning uses neural networks in order to estimate the Q-values for each action instead of a Q-table. Environments where the state and/or action space is continuous or large would make defining a Q-table too complex.

## Hyperparameters

The following values were used for the hyperparameters:

* replay buffer size - 1e5
* minibatch size - 64
* discount factor gamma - 0.99
* soft update of target parameters tau - 1e-3
* learning rate - 5e-4  
* the network is updated every 4 iterations	

## Neural network architecture

The architecture of the network consists of 3 fully connected layers, with ReLU activations. The input to the first layer is equal to the state size (37). The hidden and the output layers both have 64 units.

## Results

The environment was solved in 474 episodes, with an average score of 13.06 over the last 100 episodes. The figure below shows the plot of the rewards leading to the solution of the environment.

<img src="/score_plot.png"/>

## Future work	 	

The solution could be improved by extending the q-learning algorithm itself in its weak spots. Some of the possible approaches are:
* Double DQN: double DQN introduces the use of two Q-value estimators. Overfitting can be avoided by using the frozen wights from the secondary neural network for the test set.
* Dueling DQN: the dueling architecture explicitly separates the representation of state values and state-dependent action values via two separate streams the NN architecture. By doing this we can evaluate states, without having to check the effect of each action for each state.
* Prioritized experience replay: in experience replay prioritizing the choice of samples that stem from larger errors in the estimated values. The error is used to calculate the probability for the choice of samples, i.e. samples with larger errors have a better chance of being selected for replay.