

# AI Lunar Lander Agent with Double Deep Q-Networks

This project features an AI agent employing Double Deep Q-learning to autonomously learn how to safely land a Lunar Lander within the OpenAI universe.

## Algorithm Details and Hyperparameters

- Implementation: Keras with TensorFlow Backend
- Algorithm: Deep Q-Network (DQN) with Double Fully Connected Layers
- Neural Network Structure: Two fully connected layers, each with 128 nodes
- Optimization Algorithm: Adaptive Moment (Adam)
- Learning Rate: α = 0.0001
- Discount Factor: γ = 0.99
- Minimum Exploration Rate: ε = 0.1
- Replay Memory Size: 10^6
- Mini-Batch Size: 2^6

## Problem Description

The agent's objective is to master the safe, rapid, and accurate landing of a Lunar Lander on the moon's surface. The environment assigns negative rewards if the lander free-falls dangerously or fails to land within 20 seconds. If the lander safely touches down but in an incorrect position, it receives a small negative or positive reward, depending on its proximity to the landing zone. Successfully and safely landing the lander within the designated zone results in a highly positive reward.

## Double Deep Q Networks (DDQN)

Since the state space is infinite, traditional Q-value table methods are ineffective. Deep Q-learning combines Q-learning with neural networks to approximate Q-values. However, the action space remains discrete.

**Q-learning:** (Equation and MDP graph shown)

For Deep Q-learning, a neural network approximates Q-values in each time step and updates the network to make the estimated Q(s,a) approach its target.

**Difference between Q-learning and DQN:**

Purpose of using Double Deep Q-network:
- Stabilize the target Q-value and ensure convergence.

## Training Result

- The agent begins with noisy exploration and imperfect approximation but improves over time.
- The learning curve displays the reward earned in each episode, with the red curve indicating the moving average of rewards over 100 consecutive episodes.
- The agent successfully learns a policy to solve the Lunar Lander problem, with the average reward for any 100 consecutive episodes reaching at least 200.

The original implementation and data credits go to their respective authors. This information is presented here for personal understanding and educational purposes.