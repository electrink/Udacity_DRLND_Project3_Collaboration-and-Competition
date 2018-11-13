[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135623-e770e354-7d12-11e8-998d-29fc74429ca2.gif "Trained Agent"


# Udacity_DRLND_Project3_Collaboration-and-Competition
In this repository, I provide source codes for implementing a deep deterministic policy gradient (DDPG) algorithm to solve the Collaboration and Competition (Tennis) problem in the Unity ML-Agents environment. This is the third project of the Udacity's Deep Reinforcement Learning Nano Degree (DRLND) program.

![Trained Agent][image1]

## Environment
The environment is provided by the DRLND’s course website. In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1.  If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01.  Thus, the goal of each agent is to keep the ball in play.

The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation.  Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping. 

The task is episodic, and in order to solve the environment, your agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

- After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
- This yields a single **score** for each episode.

The environment is considered solved, when the average (over 100 episodes) of those **scores** is at least +0.5.

## Getting Started
### Prerequisites
- tensorflow==1.7.1
- Pillow>=4.2.1
- matplotlib
- numpy>=1.11.0
- jupyter
- pytest>=3.2.2
- docopt
- pyyaml
- protobuf==3.5.2
- grpcio==1.11.0
- torch==0.4.0
- pandas
- scipy
- ipykernel
- pickle
- collections
- unityagents

Note that to work properly in the Windows 7 64-bit environment, one has to mannualy place the following three folders - *unityagents*, *communicator_objects*, and *Banana_Windows_x86_64* - at the root of this working directory. This may or may not be the case for other operating systems.  

## Instructions
### Training
Open *Tennis_Jing Zhao.ipynb* to start training an AI agent. This script interacts with the Unity ML-Agents environment to gain experience which is defined by visiting a new state and receiving a reward from the previous action. In addition, the script also uses the DDPG learning algorithm implemented in *ddpg_agent_v2.py* and *model_v2.py* to improve the agent's performance over time.    

### Viewing the Result
After training is done, one can view the agent's performance across total episodes in *Tennis_Jing Zhao.ipynb*. This result is stored in the *zipScore_solved.pickle* file. The 100-point moving average of the score is also provided to illustrate that the environment is solved in 1058 episodes. The weights of trained networks are saved in files *checkpoint_actor_SOLVED_1158.pth* and *checkpoint_critic_SOLVED_1158.pth* respectively.

## Author
Jing Zhao. Implementation of the DDPG algorithm is inspired by the [Deep Deterministic Policy Gradient Algorithms (DDPG)](https://github.com/electrink/deep-reinforcement-learning/tree/master/ddpg-bipedal) project in the DRLND program.
