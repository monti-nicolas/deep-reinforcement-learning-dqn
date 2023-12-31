# deep-reinforcement-learning-navigation

## Project Details
I have worked on this project as part of the Udacity's Deep Reinforcement Learning Nanodegree program. The goal is to train an agent to navigate (and collect bananas!) in a large, square world.
This world, which we refer to as environment, is provided by Unity Machine Learning Agents (ML-Agents) - an open-source Unity plugin that enables games and simulations to serve as environments for training intelligent agents.

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of the agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. 
Four discrete actions are available, corresponding to:

* 0 - move forward.
* 1 - move backward.
* 2 - turn left.
* 3 - turn right.

The task is episodic, and in order to solve the environment, the agent must get an average score of +13 over 100 consecutive episodes.

**Note: The project environment is similar to, but not identical to the Banana Collector environment on the Unity ML-Agents GitHub page.**

## Getting Started
The README has instructions for installing dependencies or downloading needed files.

To set up your python environment to run the code in this repository, follow the instructions below.

1. Create (and activate) a new environment with Python 3.6.

* Linux or Mac:
```
conda create --name drlnd python=3.6
source activate drlnd
```
* Windows:
```
conda create --name drlnd python=3.6 
activate drlnd
```

2. Clone the Udacity repository below and navigate to the python/ folder. Then, install several dependencies.

```
git clone https://github.com/udacity/Value-based-methods.git
cd Value-based-methods/python
pip install .
```

3. Create an IPython kernel for the drlnd environment.
```
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

4. Before running code in a notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu.
(/images/ipynb-kernel.png)



## Instructions
The README describes how to run the code in the repository, to train the agent.
