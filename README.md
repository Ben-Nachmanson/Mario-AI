# Super Mario AI with Reinforcement Learning in Python

This project uses the power of reinforcement learning to train an AI model to play the classic Super Mario game. We utilize the `stable_baselines3` library, along with the Super Mario environment provided by `gym_super_mario_bros`, and efficiently run the training on Mac M1's GPU using the "mps" device in PyTorch.

## Prerequisites

- Mac with M1 chip
- Python 3.x

## Setup & Installation

1. **Install Required Libraries**:

    ```bash
    pip install stable-baselines3 gym-super-mario-bros nes-py matplotlib
    ```

2. **Enable GPU Support**:

    Our project takes advantage of the GPU capabilities of the Mac M1 for efficient training. Ensure your Python environment is set up correctly to utilize the "mps" device.

## Project Overview

1. **Setting Up Mario**: We initialize the Mario environment, simplify its controls, and apply grayscale to preprocess the visual input.

2. **Frame Stacking**: Frames from the game are stacked, allowing the AI to understand motion from static images. You can visualize the stacked frames using the provided Matplotlib code.

3. **Training the Model**: We define a custom callback to save model checkpoints at regular intervals. The model is trained using the Proximal Policy Optimization (PPO) algorithm with a specified learning rate and other parameters. Training logs are saved in a designated directory.

4. **Playing the Game**: Once trained, the model can be loaded and used to play the game. This is visualized in a loop, where the AI continuously takes actions based on its predictions until the game ends.

## How to Run

1. **Train the Model**:

    Navigate to the project directory and run your training script (assuming it's saved as `mario.ipynb`):

    ```bash
    python mario.ipynb
    ```

    The trained model and checkpoints will be saved in the designated directories.

2. **Watch AI Gameplay**:

    After training, you can watch the AI play the game by running the corresponding part of the script. If this is in a separate script, run it like:

    ```bash
    python mario.ipynb
    ```

    Enjoy the AI's gameplay as it navigates through the Super Mario levels!

## Technologies & Libraries Used

- [stable_baselines3](https://github.com/DLR-RM/stable-baselines3): Reinforcement learning library.
- [gym-super-mario-bros](https://github.com/Kautenja/gym-super-mario-bros): An OpenAI Gym environment for Super Mario Bros on the NES using the nes-py emulator.
- [PyTorch](https://pytorch.org/): The underlying deep learning library used by stable_baselines3.
- [Matplotlib](https://matplotlib.org/): For visualizing stacked frames.

## Acknowledgments

Special thanks to all open-source projects and libraries that made this project possible.
