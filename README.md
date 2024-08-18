# Flappy Bird Reinforcement Learning Agent, a Q Learning Implementation

## Overview

This project demonstrates the implementation of a Q Learning algorithm to train a Reinforcement Learning (RL) Agent that significantly outperforms human players in the game of Flappy Bird. 

The project is structured into three Jupyter Notebooks, each serving a specific purpose :

### Notebooks details

## 1 - Human Play (#flappy_bird_game_for_human.ipynb)

This notebook allows users to interact with the game manually. It serves as a baseline for comparing human performance with the one of the Q Learning Agent.

## 2 - Agent Play (#flappy_bird_game_played_by_agent.ipynb)

In this notebook, the trained Q-Learning Agent plays the game. An accelerated game is coded to showcase how the trained agent outperforms human performance.

## 3 - Training and Testing (#notebook_to_train_the_rl_agent.ipynb)

This notebook contains the core of the project.

### Key features :

- Implementation of the Q-Learning Algorithm (Bellman Equation)

- Adding the agent decision making to the previous implementation of the game

- Training the agent over multiple episode

- Testing the trained Q Table 

## Technical Details :

### Q-Learning Algorithm 

- State Representation :

A game state is defined as a 2D vector containing the vertical and horizontal distances between the bird and the next pipes opening.

- Action Space :

The agent can either "do nothing" (action=0) or jump (action=1)

- Reward Function :

The reward values 1 as long as the bird is still alive and -100 if the bird dies. It was also tested to use a reward that decreases as the vertical distance between the bird and the next pipes opening increases. Both reward seem to work.

- Hyperparameters :

We use an $\epsilon$ greedy policy to make choice. This means that we choose with probability $\epsilon$ a random action between $0$ and $1$ (with probability 1/2 each) or choose the best action according to the current Q-Table values (therefore with probability $1-\epsilon$). Epsilon has been set to $0.001$. As for the discount factor that is used in the optimization of the Q Table with the Bellman Equation, it has been set to $0.1$.


 


