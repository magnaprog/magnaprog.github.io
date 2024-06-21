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

### Cooperation Between Agents

The offensive and defensive agents work together to achieve the team’s objectives, balancing offense and defense effectively through implicit communication and shared game state.

## Evaluation and Results

To test the efficacy of our Approximate Q-Learning agents, we conducted a series of games against a team of greedy agents. Our learning-based agents significantly outperformed the greedy agents, demonstrating the potential of RL techniques in creating intelligent and adaptive agents.

### Performance Metrics

- **Blue Win Rate**: 84%
- **Tie Rate**: 14%
- **Red Win Rate**: 2%
- **Average Blue Team Win Margin**: 6.18 Pellets

## Future Work

- Further experiment with PPO implementation by optimizing hyperparameters.
- Conduct thorough testing to refine agent strategies and enable team-based decision-making.
- Explore integrating advanced learning techniques such as deep Q-networks (DQN) and Double DQN.
- Investigate the use of transfer learning and curriculum learning to improve the generalization capabilities of our agents.
- Develop real-time adaptation mechanisms for dynamic strategy adjustments.
- Expand the game environment to include more complex maps, additional game elements, and varied objectives.

## References

- Sutton, R. S., & Barto, A. G. (2018). Reinforcement learning: An introduction. MIT press.
- Mnih, V., Kavukcuoglu, K., Silver, D., et al. (2015). Human-level control through deep reinforcement learning. Nature, 518(7540), 529-533.
- Schulman, J., Wolski, F., Dhariwal, P., Radford, A., & Klimov, O. (2017). Proximal policy optimization algorithms. arXiv preprint arXiv:1707.06347.
- Lowe, R., Wu, Y., Tamar, A., et al. (2017). Multi-agent actor-critic for mixed cooperative-competitive environments. arXiv preprint arXiv:1706.02275.
- Foerster, J., Farquhar, G., Afouras, T., et al. (2018). Counterfactual multi-agent policy gradients. Proceedings of the AAAI Conference on Artificial Intelligence.
- Vezhnevets, A. S., Osindero, S., Schaul, T., et al. (2017). Feudal networks for hierarchical reinforcement learning. arXiv preprint arXiv:1703.01161.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

We would like to thank our mentors and colleagues for their valuable feedback and support throughout the development of this project.

## Authors

- Yu-Hsin Weng - [yuhsin1614@ucla.edu](mailto:yuhsin1614@ucla.edu)
- Kevin Lee - [kevinlee69720@g.ucla.edu](mailto:kevinlee69720@g.ucla.edu)
- Varun Kumar - [vvkumar1@g.ucla.edu](mailto:vvkumar1@g.ucla.edu)
- Siddarth Chalasani - [darthsid2000@g.ucla.edu](mailto:darthsid2000@g.ucla.edu)
