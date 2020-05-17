[//]: # (Image References)

[trained_agent]: bananas.gif "Trained Agent"

# Project 1: Navigation

### Introduction

This project implements a DQN agent capable of navigating a large square world, while collecting yellow bananas and avoiding blue bananas.

![Trained Agent][trained_agent]

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of the agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

### Getting Started

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux_NoVis.zip) to obtain the environment.

2. Place the file in the same folder as the `Navigation.ipynb` file, and unzip (or decompress) the file. 

### Instructions

To set up your python environment to run the code in this repository, follow the instructions below.

1. Create (and activate) a new environment with Python 3.6.

	- __Linux__ or __Mac__: 
	```bash
	conda create --name drl python=3.6
	conda activate drl
	```
	- __Windows__: 
	```bash
	conda create --name drl python=3.6 
	activate drl
	```
	
2. Navigate to the location where you cloned this repository, and install the python dependencies.
    ```bash
    pip install .
    ```

3. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drl` environment.  
    ```bash
    python -m ipykernel install --user --name drl --display-name "drl"
    ```

4. Before running code in a notebook, change the kernel to match the `drl` environment by using the drop-down `Kernel` menu. 

5. Follow the instructions in `Navigation.ipynb`:
    - Cells in sections 1, 2 and 3 will allow you to initialize and explore the environment
    - Cells in section 4 include the training of the agent
    - Cells in section 5 include the testing of the trained agent. A saved model weights of a successfully trained agent are included in this repository as well (`weighhts.pth`), so you can skip training and go straight to this section to see a trained agent perform.

