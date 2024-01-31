# deep-reinforcement-learning-dqn

## Project Overview
I have worked on this project as part of the Udacity's Deep Reinforcement Learning Nanodegree program. The goal is to train a group of agenta to maintain its position at the target location for as many time steps as possible.
The environment is provided by Unity Machine Learning Agents (ML-Agents) - an open-source Unity plugin that enables games and simulations to serve as environments for training intelligent agents. 
For this particular implementation, I have decided to use an environment that contains 20 identical agents.

![Alt](/images/reacher.environment.png)

A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of each agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

The task is episodic, and in order to solve the environment, the agents must get an average score of +30 (over 100 consecutive episodes, and over all agents).

On this repository you will find the following:
* Continuous_Control.ipynb: Contains all the code that was used to successfully trained the agents that were able to solve this environment.
* checkpoint_actor_ddpg.pth: The saved model weights for the actor neural network.
* checkpoint_critic_ddpg.pth: The saved model weights for the critic neural network.
* Report.pdf: Provides a description of the implementation.
<br>
<br>
<br>
## Python Environment Setup
To set up your python environment to run the code in this repository, follow the instructions below.

### 1. Create (and activate) a new environment with Python 3.6.

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

### 2. Clone the Udacity repository below and install several dependencies.

```
git clone https://github.com/udacity/Value-based-methods.git
cd Value-based-methods/python
pip install .
```
The above code will try to install all packages under \Value-based-methods\python\requirements.txt. 
If you run into any issues when trying to install torch==0.4.0 then you can instead install torch by running the below code:
```
pip install torch===0.4.0 -f https://download.pytorch.org/whl/torch_stable.html
```

If you had this issue with torch==0.4.0 then don't forget to install the remaining packages from the requirements.txt file that came after torch==0.4.0: pandas, scipy and ipykernel. 

Finally, it seems that some packages were missing on the requirements.txt and are required to run some modules on the Udacity repository.
So, I would recommend to install the following:
```
pip install --upgrade google-api-python-client
python -m pip install grpcio
python -m pip install grpcio-tools
pip install Pillow
```

### 3. Create an IPython kernel for the drlnd environment.
```
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

### 4. Download the Unity Environment
For this project, you will not need to install Unity - this is because Udacity has built the environment for you, and you can download it from one of the links below.
You need only select the environment that matches your operating system:

* Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
* Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
* Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
* Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

Then, place the file in the p2_continuous-control/ folder from cloned Udacity GitHub repository, and unzip (or decompress) the file.
<br>
<br>
<br>
## Getting Started
Once the Python environment has been setup, all dependencies were installed and the Reacher environment has been downloaded then you should be ready to get started to interact with the environment and train your agents.
To do this, open the Continuous_Control.ipynb within the cloned Udacity repository and run the code cells to get familiar on how to interact with the environment.

**Note: Before running code in a notebook, don't forget to change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu:**

![Alt](/images/ipynb-kernel.png)

Alternatively, you can download the Continuous_Control.ipynb from this repository into your locally cloned version of the Udacity repository which will give you an overview of a successfully DDPG implementation.
Hopefully this will give you a starting point to make your own adjustments.


