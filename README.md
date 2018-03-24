# RL-Q-learning-8puzzle-Pytorch
This is a project using neural-network reinforcement learning to solve the 8 puzzle problem (or even N puzzle)

If you want to know what is the 8 puzzle problem, please look at:
http://coursera.cs.princeton.edu/algs4/assignments/8puzzle.html

https://en.wikipedia.org/wiki/15_puzzle

If you need some background on the Q learning and deep Q learning, here is a good references:
http://outlace.com/rlpart3.html

If you want to know how to use Pytorch to do reinforcement learning, please refer to the Pytorch tutorial:
http://pytorch.org/tutorials/intermediate/reinforcement_q_learning.html

This project contains two files: `n_puzzle.py` is for constructing a 8 puzzle game, and `DQN.py` is used to construct and train the neural network. Since I use the Pytorch to construct the network, I also use the tensor of Pytorch for constructing the game. If you are only interested in the 8 puzzle game, please download the Pytorch before implementing the `n_puzzle.py`. Of cause, you can always change the Pytorch Tensor into numpy Array.


Tutorial:

First, import both files:

`from n_puzzle import N_puzzle`

`from DQN import hidden_unit, Q_learning, RL_training`

Then, construct the network and traning system:

`network = Q_learning(72, [250,250], 4, hidden_unit)`

`train = RL_training(3, 10, network, epsilon = 0.9, gamma = 0.9, lr = 1e-4)`

The last step is to train and test the DQN:

`train.train(10001,1000)`

`train.test()`

Given the above parameters and training, the network can achieve 75% success rate to solve a 8 puzzle in 20 steps. The difficulty (manhattan distance of the starting puzzle) is 10. If you give such a puzzle to a human and ask him/her to solve in 20 steps, it is likely that they would fail. After fine tuning and more traning, the success rate can reach 85%, which is smart enough compared to me.