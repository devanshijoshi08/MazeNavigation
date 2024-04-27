# Comparative Analysis of Reinforcement Learning Algorithms in a Maze Environment

## Project Overview
This project involves a detailed comparative analysis of three prominent reinforcement learning algorithms—SARSA, Q-Learning, and Dyna-Q—in navigating complex gym-maze environments. Our aim is to identify the most efficient algorithm for pathfinding tasks by evaluating performance metrics such as number of steps to the goal, success rate, learning speed, and total accumulated rewards across various maze configurations.

## Table of Contents
- [Introduction](#introduction)
- [Environment Setup](#environment-setup)
- [Implementation](#implementation)
- [Results and Discussion](#results-and-discussion)
- [Conclusion and Future Work](#conclusion-and-future-work)

## Introduction
This section introduces the problem of maze navigation and the relevance of using reinforcement learning algorithms to solve such problems. The maze challenges include obstacles, varying path lengths, dead-ends, and additional complexities like portals and loops.

## Environment Setup
We used a gym-maze environment which is a 10x10 grid with various configurations. The detailed settings for the maze can be viewed at: [Gym-Maze Repository](https://github.com/MattChanTK/gym-maze).

### Configuration Details
- **Standard Maze (10x10)**: Basic setup with predefined start and goal positions.
- **Complex Mazes (10x10)**: Setup of mazes which include portals and loops. 

## Implementation
This project was implemented using Python, with reinforcement learning environments managed through OpenAI's Gym interface. Each algorithm was tuned with specific parameters:
- **Learning Rate (Alpha)**
- **Discount Factor (Gamma)**
- **Exploration Rate (Epsilon)**

Scripts and detailed parameter settings can be found in the `code` directory of this repository.

## Results and Discussion
The results are extensively discussed in the report with corresponding plots showing the performance of each algorithm across different maze setups. Summaries of these findings include:
- Performance metrics over episodes
- Comparisons of learning rates, success rates, and optimization of pathfinding strategies.

For detailed plots and a full discussion, refer to the [Results Section](#results-and-discussion) of this document.

## Conclusion and Future Work
The study concludes that while each algorithm has its strengths, certain configurations such as the Dyna-Q with simulated planning show promise for complex maze environments. Future work could explore the integration of these algorithms with deep learning approaches to tackle even more challenging navigation problems.

### Potential Extensions
- **Hybrid Algorithms**: Combining classical RL algorithms with neural networks.
- **Real-world Applications**: Applying the insights gained to physical robots in maze-like environments.