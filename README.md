# Flappy-bird
a self project to play flappy bird game
Project Objective: Developing an autonomous agent to play Flappy Bird using Reinforcement Learning (Q-Learning).

Physics Engine & Game Foundations The first phase focused on implementing the core game mechanics using Python and Pygame.
Vertical Dynamics: Developed a physics function where the bird's vertical position is updated based on a gravity constant and upward velocity (flapping).

Collision Detection: Implemented logic to track boundaries for the ground and pipe obstacles.

Vectorized Math: Used NumPy to handle state calculations efficiently and Matplotlib to build the framework for visualizing training rewards.

Environment Design (MDP) To prepare for Reinforcement Learning, I formalized the game as a Markov Decision Process (MDP).
State Representation: Defined a 4-dimensional state vector to ensure the Markov property: (bird_y, velocity, distance_to_pipe, gap_offset).

Discretization: Since Tabular Q-Learning requires a finite state space, I implemented a "binning" logic. This converts continuous pixel values into discrete categories (e.g., bird position relative to the gap: above, inside, or below). This step is critical to prevent the Q-table from becoming unmanageably large.

Reward Structure & Validation I explored different reward strategies to guide the agent’s learning:
Sparse vs. Dense Rewards: Tested simple goal-based rewards (+10 for passing pipes) against dense rewards (+0.1 for survival) to provide constant feedback to the agent.

Random Policy Testing: Validated the environment by running a random action policy for 500 episodes. This confirmed that the physics and collision logic work as intended, providing a baseline survival rate of ~15-20 steps.

Current Progress Summary Week 1 Assignments: Completed foundational Python logic, class structures, and Pygame physics.
Week 2 Assignments: Successfully built the FlappyEnv class, implemented discretization, and performed environment stress testing.

Next Steps The next phase will involve implementing the Q-Learning algorithm, initializing the Q-table, and beginning the training process to improve the bird's performance beyond the random baseline.
Learning: I learned how sensitive RL agents are to reward scaling.

Next Steps Implement the Q-Learning algorithm.
Begin training the agent and tuning hyperparameters.

Analyze the learning curve using Matplotlib.
