# Deep-Q-Networks-RL
<h2>Goal: </h2>

* The goal is to work with value function approximation algorithms (i.e. Deep Q-learning (DQN)), to explore OpenAI Gym environments, and improve the vanilla DQN algorithm to understand the benefits of approximation methods, the role of deep neural networks as well as some of the techniques used in practice to stabilize training and to achieve better performance.

<h2>Part 1 </h2>

I explored 'CartPole-v1' and 'Mountain Car v0' environments. Below are few details of the environments.

<h3>Cart pole v1:</h3>

* Cart pole v1 main details:
  * Goal: To keep the pole upright.
  * Actions:
    0: Left
    1: Right
* Observation space:
  * (Observation, Min, Max):
  1. (Cart Position, -4.8, 4.8)
  2. (Cart Velocity, -Inf, Inf)
  3. (Pole Angle, ~ -0.418 rad (-24°), ~ 0.418 rad (24°))
  4. (Pole Angular Velocity, -Inf, Inf)
* Rewards:
   * Reward of +1 for every step taken including the termination step, is allotted. The threshold for rewards is 475 for v1.
* Initial State:
   * All observations are assigned a uniformly random value in (-0.05, 0.05)
* Episode Termination Conditions:
    1. Pole Angle is greater than ±12°
    2. Cart Position is greater than ±2.4 (center of the cart reaches the edge of the display)
    3. Episode length is greater than 500 (200 for v0)
    
<h3>Mountain Car v0:</h3>

* Goal: The goal is to reach the flag placed on top of the right hill as quickly as possible.
* Actions:
  1. Accelerate to the left
  2. Don't accelerate
  3. Accelerate to the right
* Observation space:
  1. Position of the car along the x-axis
  2. Velocity of the car
* Reward:
  * 0: if it takes step towards the goal.
  * -1: if it takes step that isn't towards the goal
* Initial State:
  * The position of the car is assigned a uniform random value in [-0.6, -0.4]. The starting
  velocity of the car is always 0.
* Episode Termination Conditions:
  1. The position of the car is greater than or equal to 0.5 (the goal position on top of the right
  hill)
  2. The length of the episode is 200.
  
  
<h2>Part 2:</h2>

  * Implemented DQN from scratch following DeepMind’s paper (<small>[Nature paper](https://web.stanford.edu/class/psych209/Readings/MnihEtAlHassibis15NatureControlDeepRL.pdf)</small> and <small>[initial version](https://arxiv.org/pdf/1312.5602.pdf)</small>) using Keras.
  * Solved Grid-world,  'CartPole-v1' and 'MountainCar-v0' environments using DQN algorithm, results are impressive (i.e. refer report for more details)
  
 <h2>Part 3:</h2>
 
  * Implemented Double DQN (i.e. improvement) to vanilla DQN algorithm.
  * I have implemented Double DQN as it reduces the overestimation problem, for this I have changed my target value calculation and syncing weights strategy.
  * Solved Grid-world, Open AI 'CartPole-v1' and 'MountainCar-v0' environments. 
  * Compared results from vanilla DQN and improved version to get an intuition about how RL agent is learning in complex environments.
  
