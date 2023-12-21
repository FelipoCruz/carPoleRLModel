## Step 1: Set Up Your Environment

Ensure you have Python installed on your computer. Python 3.6 or later is recommended.
Install the required Python packages: gymnasium, numpy, and matplotlib. You can do this using pip:
pip3 install gymnasium numpy matplotlib
pip3 install 'gymnasium[classic-control]'

## Step 2: Prepare the Script

Copy the provided script into a text editor.
Save the file with a .py extension, for example, main.py.

## Step 3: Running the Script

Open a terminal or command prompt.
Navigate to the directory where you saved main.py.
Run the script using Python:
python3 main.py

## Understanding the Script

The script contains a function run that can train a new agent or use a pre-trained agent to play the game.
By default, the function run(is_training=False, render=True) is called, which will load a pre-trained model (cartpole.pkl) and display the game window. If cartpole.pkl does not exist, you should train the model first by calling run(is_training=True, render=False).
The training process involves Q-learning, a reinforcement learning algorithm, and the agent learns to balance the pole on the cart.
The script uses Gymnasium's 'CartPole-v1' environment as the training and testing ground.
If render=True, the script will visually render the game environment. For training (is_training=True), you might want to set render=False for faster execution.

## Note:

If you haven't trained the model yet (i.e., there's no cartpole.pkl file), you need to run the script with is_training=True first. This process can take some time depending on your computer's processing power.
Ensure that your system meets the requirements for running graphical simulations if you enable render=True.
The script will automatically save the trained model to cartpole.pkl and a plot of the training progress to cartpole.png.
Running the script as-is will attempt to use a pre-trained model. If you want to train the model from scratch, you'll need to change the last line in the script to run(is_training=True, render=False) and then run the script again.
