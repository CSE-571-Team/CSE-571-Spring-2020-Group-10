# CSE-571-Spring-2020-Group-10

## Project topic 5. Reinforcement Learning agent in Wumpus world

### How to run the project

The project for implementing the Q-Learning agent is built on the Wumpus Hybrid Agent Project. Thus the project supports the Hybrid Agent and Reinforcement learning agent based on Q-Learning 

#### Hybrid agent

1. The following command runs the hybrid agent in default layout

   ```shell
   python wumpus.py -y
   ```

2. The following command runs the hybrid agent in a user defined layout 

   -l option specifies the option to give a user defined layout file. The layout file should be present in the layout folder.

```shell
python wumpus.py -y -l wumpus_4x4_1
```

#### Q Learning Agent

1. The following command runs the Q learning agent in default layout with default parameters

   ```shell
   python wumpus.py -q
   ```

2. The following command runs the Q learning agent in a user defined layout 

   -l option specifies the option to give a user defined layout file. The layout file should be present in the layout folder. 

```shell
python wumpus.py -y -l wumpus_4x4_1
```

3. Learning parameters can be specified in the following format

   -s specifies stochasticity with stochastic parameters [0.1,0.8,0.1]. If agent tries to move forward, it will move in the forward location with probability 0.8 and with probability 0.1 in the left and right location respectively. While specifying this in the parameter, there should be no space inside the square brackets.

   -g represents the discount factor (gamma)

   -a represents the learning rate (alpha)

   -e represents the exploration factor (epsilon)

   -x represents the maximum number of training agent receives. Agent will stop after training after it reaches this value even if does not reach the convergence 

   -m represents the minimum number of training agent receives before it starts checking for convergence

   -d represents the maximum deviation in the Q value. The agent will compare the previous Q values with the current updated Q values for all actions it performs in the environment for a given episode. If all Q value updates are less, than agent will compare the previous policy with the current policy. If both policies match then agent will stop its training

   -r represents the number of runs agent will perform after the policy has been generated. Average score after running this many runs by the agent will be printed

   ```shell
   python wumpus.py -q -s [0.1,0.8,0.1] -g 0.8 -a 0.2 -e 0.05 -x 123 -m 12 -d 0.0004 -r 70
   ```

   