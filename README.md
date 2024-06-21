# Capture The Flag Pacman with Reinforcement Learning

## Overview

This project presents the development and implementation of a Capture The Flag (CTF) variation of Pacman using both non-ML (greedy algorithms) and ML approaches for agent behavior. We employ reinforcement learning (RL) algorithms such as Q-Learning and Proximal Policy Optimization (PPO) to enable adaptive agent strategies. This interdisciplinary project integrates machine learning, game development, and animation concepts, making it highly relevant to the study of artificial life for computer graphics and vision.

## Motivation

The primary motivation for this project is to simulate real-world cooperation through a CTF variation of Pacman. By leveraging RL algorithms, our agents learn and adapt their strategies over time, providing valuable insights into multi-agent systems exhibiting life-like behaviors. This project has practical applications in robotics, autonomous systems, and game development, utilizing Unity for visualization and integrating concepts from machine learning and artificial life.

## Features

- **Game Engine**: Manages the overall game state, including the positions and states of the agents, and handles interactions between agents.
- **Action Models**: Incorporates both non-ML (greedy algorithms) and ML-based (reinforcement learning) action models for making informed decisions based on the current game state.
- **Integration into Unity**: Utilizes ONNX models to transport trained RL models from Python to Unity, enabling real-time decision-making within the game environment.
- **Adaptive Agent Strategies**: Implements RL algorithms such as Q-Learning and PPO to develop intelligent agents capable of learning and adapting their behaviors.

## Agent Design and Implementation

### Offensive Agent

The Offensive Agent is responsible for capturing pellets on the enemy’s side and delivering them back to the home side. The agent uses Approximate Q-Learning, leveraging a set of carefully chosen features to guide its decision-making process.

#### Features

- Bias
- Distance to Nearest Pellet
- Eats Food
- Distance to Nearest Capsule
- Eats Capsule
- Distance to Home
- Number of Ghosts Within Two Steps

### Defensive Agent

The Defensive Agent aims to protect its side by preventing the opposing team’s Pacman agents from capturing pellets. This agent also uses Approximate Q-Learning, with features designed to detect and intercept enemy agents.

#### Features

- Number of Invaders
- Distance to Invaders
- On Defense
- Stop and Reverse Penalties

### Performance Metrics

- **Blue Win Rate**: 84%
- **Tie Rate**: 14%
- **Red Win Rate**: 2%
- **Average Blue Team Win Margin**: 6.18 Pellets
