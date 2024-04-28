# Comparative Analysis of Reinforcement Learning Algorithms in a Maze Environment

## Project Overview
Our project aims to perform a thorough evaluation of reinforcement learning algorithms, such as Q-Learning, SARSA, and Dyna, with a particular focus on how well they solve problems in the gym-maze setting. Our objective is to evaluate the shortest path finding performance, learning rate, and changeability of various algorithms in a 10x10 maze and potentially with some complex mazes. We aim to understand their methods and flexibility by comparing their performance indicators, which include the number of steps they took to attain the goal, the awards they accumulated, and the total time efficiency. 
This analysis will help optimize pathfinding tactics in dynamic environments by highlighting the advantages and disadvantages of each algorithm as well as provide insights on how to apply them in difficult decision-making scenarios.

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
SARSA:
-	SARSA with decaying exploration rate (epsilon) performed the best, demonstrating a strong balance between exploration and exploitation over time.
-	Exhibited quick convergence to a stable and efficient policy, with a notable decrease in the number of steps to reach the goal.
-	Maintained consistent performance throughout the episodes, signifying effective learning and policy optimization.
-	Demonstrates rapid policy convergence in complex mazes, with decaying exploration significantly reducing steps to goal.

Q-Learning:
-	The adaptive learning rate variation of Q-Learning showed impressive performance, adapting the learning rate based on the episode progression for optimal updates to Q-values.
-	Achieved a rapid increase in total rewards and a substantial decline in the number of steps required to solve the maze, indicating swift learning.
-	Presented a steady average reward per step, implying the agent’s ability to refine its policy for maximum efficiency.
-	Shows strong adaptability with dynamic learning rates, quickly maximizing rewards and efficiently solving mazes.

Dyna-Q:
-	Dyna-Q with the exploration component added into the planning phase proved to be highly effective, allowing the agent to explore multiple strategies rapidly.
-	This variation displayed a quick learning curve with an immediate decrease in steps per episode, pointing to an effective strategy acquisition.
-	There was a quick stabilization in the total rewards and a consistent average reward per step, showcasing the agent’s ability to efficiently navigate the maze.
-	Excels with simulated planning, rapidly integrating portals and loops into its navigation strategy for effective maze traversal.

Cross-Algorithm Comparison:
-	SARSA and Dyna-Q variations with decaying rates (epsilon for SARSA and learning rate for Dyna-Q) showed a more exploratory early learning phase followed by an exploitation-focused approach, which was effective in maze navigation.
-	Q-Learning's adaptability through a dynamic learning rate highlighted its robustness in achieving and maintaining high performance with less concern for the balance between exploration and exploitation, as opposed to the more nuanced approach in SARSA and Dyna-Q.
-	Dyna-Q's incorporation of simulated experiences provided it with a unique advantage, allowing it to perform well despite less focus on exploration in the real environment compared to SARSA.

Algorithm Selection:
-	Dyna-Q's ability to adapt to mazes with unique features like portals and loops, coupled with its simulated experience planning, suggests a superior approach for complex navigation tasks.
-	Overall, while each algorithm has its strengths, Dyna-Q’s dual approach of learning from both real and simulated experiences appeared to provide a slight edge in terms of speed and efficiency in learning the optimal policy for the maze navigation task.


## Conclusion and Future Work
The study concludes that while each algorithm has its strengths, certain configurations such as the Dyna-Q with simulated planning show promise for complex maze environments. Future work could explore the integration of these algorithms with deep learning approaches to tackle even more challenging navigation problems.

### Potential Extensions
- **Hybrid Algorithms**: Combining classical RL algorithms with neural networks.
- **Real-world Applications**: Applying the insights gained to physical robots in maze-like environments.