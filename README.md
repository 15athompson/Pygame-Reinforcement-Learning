# Teach AI To Play Snake! Reinforcement Learning With PyTorch and Pygame


- Part 1: Setup the environment and implement the Snake game.
- Part 2: Implement the agent that controls the game.
- Part 3: Implement the neural network to predict the moves and train it.

Role: Snake Game AI Agent

Description:
This is an implementation of a Snake Game AI agent using reinforcement learning techniques. The agent is designed to play the classic Snake game autonomously. Here is a summary of the key components and functionalities of the code:

Imports: The code imports necessary libraries and modules including torch, random, numpy, and custom modules for the game (game.py), the neural network model (model.py), and helper functions (helper.py).

Hyperparameters: Several hyperparameters are defined at the beginning of the code, including MAX_MEMORY for memory management, BATCH_SIZE for training batch size, and LR for the learning rate.

Agent Class: The core functionality is encapsulated within the Agent class. The agent is responsible for controlling the snake in the game.

Game State Representation: The get_state method calculates the state of the game based on the snake's position, potential dangers, movement direction, and food location. It returns a numeric array representing the state.

Memory Management: The agent maintains a memory buffer using a deque to store past experiences, including the state, action, reward, next state, and whether the game is done.

Training: The agent trains using two methods: train_long_memory and train_short_memory. train_long_memory performs training on batches of experiences, while train_short_memory updates the neural network after each game step.

Action Selection: The get_action method chooses the snake's next move. It balances exploration and exploitation by using an epsilon-greedy approach. It selects a random action with a decreasing probability (epsilon) or chooses the action with the highest predicted Q-value.

Training Loop: The train function contains the main training loop. It initializes the game, plays the game, and trains the agent based on the game's outcomes. It also keeps track of the agent's performance over multiple games.

Recording and Plotting: The code records and plots game scores, maintains a record of the highest score achieved, and saves the model when a new record is set.

Main Entry Point: The if __name__ == '__main__': block ensures that the train() function is executed when the script is run.

This code trains a Snake Game AI agent using reinforcement learning, balancing exploration and exploitation to maximize the agent's performance in the game. 
