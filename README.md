# deep-reinforcement-learning-navigation

## Project Overview
I have worked on this project as part of the Udacity's Deep Reinforcement Learning Nanodegree program. The goal is to train an agent to navigate a large square world to collect yellow bananas while avoiding blue bananas.
This world, which we refer to as environment, is provided by Unity Machine Learning Agents (ML-Agents) - an open-source Unity plugin that enables games and simulations to serve as environments for training intelligent agents.

![Alt](/images/banana-world.png)

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of the agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. 
Four discrete actions are available, corresponding to:

* 0 - move forward.
* 1 - move backward.
* 2 - turn left.
* 3 - turn right.

The task is episodic, and in order to solve the environment, the agent must get an average score of +13 over 100 consecutive episodes.

On this repository you will find the following:
* Navigation.ipynb: Contains all the code that was used to successfully trained an agent that was able to solve this environment.
* checkpoint.pth: The saved model weights of the successful agent.
* Report.pdf: Provides a description of the implementation.

**Note: The project environment is similar to, but not identical to the Banana Collector environment on the Unity ML-Agents GitHub page.**
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

* Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
* Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
* Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
* Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

Then, place the file in the p1_navigation/ folder from cloned Udacity GitHub repository, and unzip (or decompress) the file.
<br>
<br>
<br>
## Getting Started
Once the Python environment has been setup, all dependencies were installed and the Banana environment has been downloaded then you should be ready to get started to interact with the Banana environment and train your agent.
To do this, open the Navigation.ipynb within the cloned Udacity repository and run the code cells to get familiar on how to interact with the environment.

**Note: Before running code in a notebook, don't forget to change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu:**

![Alt](/images/ipynb-kernel.png)

Alternatively, you can download the Navigation.ipynb from this repository into your locally cloned version of the Udacity repository which will give you an overview of a successfully trained agent.
Hopefully this will give you a starting point to make your own adjustments.


