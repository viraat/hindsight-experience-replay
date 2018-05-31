# hindsight-experience-replay

Reproducing results from the [Hindsight Experience Replay](https://arxiv.org/abs/1707.01495) Paper in [PyTorch](https://pytorch.org/)

## Details
* implemented the bit flip environment
  *  Task: given a starting string of `n` bits and a target string of same length, flip the bits in the start string till the target string is achieved. The number of flips allowed is equal to the number of bits in the string - `n`
* implemented a deep q-network with one hidden layer of 256 nodes
* implemented hindsight-experience-replay with goal selection rule of `s_T`, i.e. the new goal is the last state achieved in the sequence of flips (in the file [dqn-her.ipynb](dqn-her.ipynb))
* implemented a baseline DQN network without hindsight-experience-replay (in the file [dqn.ipynb](dqn.ipynb))

## Results
* Compared success rate across number of episodes for bit length `n=6,7,8` for both DQN and DQN+HER (could not do higher bit length as no GPU)

![6dqn](/plots/6_dqn.png) ![6her](/plots/6_her.png)
![7dqn](/plots/7_dqn.png) ![7her](/plots/7_her.png)
![8dqn](/plots/8_dqn.png) ![8her](/plots/8_her.png)
![10her](/plots/10_her.png) ![10herloss](/plots/10_loss_her.png)
## To do
* Higher bit length using Google Colab notebook
