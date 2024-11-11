# Mario Reinforcement Learning Agent

This repository contains a Deep Q-Network (DQN) reinforcement learning agent trained to play **Super Mario Bros** using the `gym_super_mario_bros` environment in Python with PyTorch.

## Project Structure

- **`main.py`**: Main training script for the Mario agent. Configurable to start training from scratch or to load a pre-trained model. It saves model checkpoints periodically.
- **`agent.py`**: Defines the `Agent` class. This includes the DQN-based Mario agent, epsilon decay for exploration, replay buffer, and learning routine.
- **`agent_nn.py`**: Contains the `AgentNN` class, which defines the Convolutional Neural Network used by the agent to process game frames and predict Q-values for each action.
- **`generate_clips.py`**: Script for capturing gameplay frames and actions, which are saved as image files for visualization and review.
- **`utils.py`**: Utility functions, including a `Timer` class for performance logging and a function to generate timestamped directories for saving models.
- **`wrappers.py`**: Custom environment wrappers, including frame skipping, grayscale conversion, and frame stacking to process frames efficiently.

## Features

- **Training**: The agent is trained using a DQN with a replay buffer and target network for stability.
- **Action Logging**: Logs frames and actions to visualize Mario’s gameplay and decision-making over time.
- **Customizable Parameters**: The number of episodes, checkpoint saving intervals, and epsilon decay settings are adjustable in `main.py`.
- **CUDA Support**: Automatically uses GPU if available, ensuring faster training.

## Getting Started

### Requirements

- Python 3.8+
- `torch`
- `gym_super_mario_bros`
- `nes_py`
- `Pillow`
