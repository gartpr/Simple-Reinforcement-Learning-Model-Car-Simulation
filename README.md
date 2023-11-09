# Car Racing with RLlib

This project demonstrates how to train a reinforcement learning model using RLlib (Reinforcement Learning Library) to play a simple car racing game in a custom Gym environment. The game environment is implemented in a Jupyter Notebook.

## Table of Contents
1. [Introduction](#introduction)
2. [Dependencies](#dependencies)
3. [Gym Environment](#gym-environment)
4. [Testing the Environment](#testing-the-environment)
5. [Initialize Ray](#initialize-ray)
6. [Training with RLlib](#training-with-rllib)
7. [Using the Trained Model](#using-the-trained-model)

## Introduction
In this project, we build a custom Gym environment called `Car_v0` to simulate a car racing game. The car can take three actions: slow down, maintain speed, or speed up. The goal is to keep the car's speed within the optimal range to maximize rewards. We use RLlib to train a reinforcement learning model to control the car's actions.

## Dependencies
Before running the code, ensure you have the necessary dependencies installed. You can install them using pip:

```
!pip install ray[rllib]
!pip install tensorflow
!pip install gym
!pip install numpy
```

## Gym Environment
The Car_v0 Gym environment is defined in the notebook. It simulates a car's speed, which can vary from 0 to 100. The car starts at a random speed between 52 and 62 and has a fixed driving time of 60 seconds. The reward is based on the car's speed, with positive rewards given for speeds between 57 and 61.

## Testing the Environment
We test the environment by running the car through 10 episodes with random actions. The scores (rewards) for each episode are printed, showing the car's performance.

## Initialize Ray
We initialize the Ray library, which is used for distributed computing in RLlib. Ray allows us to efficiently train reinforcement learning models.

## Training with RLlib
We register the Car_v0 environment to be used with RLlib and create a PPO (Proximal Policy Optimization) trainer. We then train the model for 20 iterations, printing the minimum, mean, and maximum rewards achieved during training. The trained model is saved for later use.

## Using the Trained Model
We load the trained model, and the car plays the game for 10 episodes. The scores achieved by the trained model are printed, demonstrating that it performs well in the game.

This README provides an overview of the project. To run and experiment with the code, please refer to the Jupyter Notebook for a more detailed step-by-step explanation and execution. Enjoy experimenting with reinforcement learning and car racing!
