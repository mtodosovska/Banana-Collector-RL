# README

This project is an implementation of a Reinforcement Learning solution to the Unity Banana Collector environment. The environment contains blue and yellow bananas. The task is to teach the agent to collect the yellow bananas and avoid the blue ones. The action space is descrete, and containes 4 possible actions. The state space has 37 dimensions. The task is episodic, and the environment is considered solved when the agent can get an average score of +13 over 100 consecutive episodes.


# Getting Started

The solution (including installing necessary packages, initialising the environment, and training the agent) can be executed by running the Navigation.ipynb file.

# Project files

The project consists of the model.py and agent.py files, as well as the Navigation.ipynb notebook. They are organized as follows:
* model.py containes the code for the neural network.
* agent.py represents the agent itself. Here the Q-learning logic is implemented. 
* Navigation.ipynb containes the code for installing the neccessary libraries, importing them, initialising the environment, agent and model, and training and saving the model weights.


