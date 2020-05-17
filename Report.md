[//]: # (Image References)

[rewards_plot]: rewards-plot.png "Rewards Plot"
[trained_agent]: bananas.gif "Trained Agent"

# Project report

## Learning algorithm

The learning algorithm used is Deep Q Learning, very similar to the one used to solve the `LunarLander` Gym environment in the [implementation](https://github.com/udacity/deep-reinforcement-learning/tree/master/dqn/solution) provided by Udacity.

The neural network implemented consists of three layers:

- Fully connected layer - input: 37, output: 64
- Fully connected layer - input: 64, output: 64
- Fully connected layer - input: 64, output: 4

The input and output correspond to the state space size (37) and action space size (4)

### Hyperparameters
Parameter | Value
--- | ---
replay buffer size | 100000
batch size | 64
gamma | 0.99
tau | 0.001
learning rate | 0.0005
update every | 4
num episodes | 1000
epsilon start | 1.0
epsilon end | 0.01
epsilon decay | 0.995

## Results

### Plot of Rewards

The environment was solved in 494 episodes, but the agent continued to be trained for 1000 episodes.
![Rewards Plot][rewards_plot]

```
Episode 100	Average Score: 0.62
Episode 200	Average Score: 3.66
Episode 300	Average Score: 7.09
Episode 400	Average Score: 10.28
Episode 494	Average Score: 13.06
Environment solved in 494 episodes!	Average Score: 13.06
Episode 500	Average Score: 13.32
Episode 600	Average Score: 14.40
Episode 700	Average Score: 15.80
Episode 800	Average Score: 14.76
Episode 900	Average Score: 14.47
Episode 1000	Average Score: 15.58
```

### Trained agent

![Trained Agent][trained_agent]

## Ideas for future work

I would like to try the following extensions:
- Double DQN
- Prioritized Experience Replay
- Dueling DQN

I would also like to solve the problem where the state is an image corresponding to the agent's first-person view of the environment.