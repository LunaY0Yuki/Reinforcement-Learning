# MountainCarContinuous Problem

### Getting Started
The environment to the MountainCarContinuous is described [here](https://github.com/openai/gym/wiki/MountainCarContinuous-v0).

### Solution Video
[![LunarLanderContinuous-v2](http://img.youtube.com/vi/RGKRfxfEFEA/0.jpg)](https://www.youtube.com/watch?v=RGKRfxfEFEA "MountainCarContinuous-v0")

The video shows the solution of the environment after 32 episodes.

### Solution Info
My learning algorithm is a Deep Deterministic Policy Gradient.

DDPG is an actor-critic algorithm and primarily uses two neural networks.
One for the actor and one for the critic. These networks calculate action vectors for the current state and and generate a temporal-difference error signal each time step.

DDPG uses a stochastic behavioral policy for good exploration and a deterministic target policy for estimating.

The current state is the input of the actuator network and the output is a single value representing the action. The deterministic policy gradient theorem provides the update rule for the weights of the actor network.

The critic's output is simply the estimated Q-value of the current state and the action given by the actor. The critic network is updated from the gradients obtained from the TD error signal.

More general information about DDPG in [this](https://arxiv.org/pdf/1509.02971.pdf) paper.

### Instructions

start Jupyter Notebook `MountainCarContinuous-v0 (DDPG).ipynb` and follow the instructions. 