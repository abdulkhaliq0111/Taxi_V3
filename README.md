# Q-Learning-Taxi-v3

- **Goal:** Obtain a *Q-Learning table* with the optimal values for the Taxi-v3 problem.
- **Approach:** Since the goal is to obtain the optimal values for the Q-table, I have implemented an *exploration-only strategy*, namely *random exploration*. Tune alpha, gamma, and/or epsilon using a decay over episodes
- **Correlated Problem:** If the goal was to learn the optimal policy as quick as possible there would be the need to implement a *exploration-exploitation strategy*, such as epsilon-greedy algorithm **[1]**.

### Taxi-v3: Open AI Gym
- **Open AI Gym:** [Gym](https://gym.openai.com/) is a toolkit for developing and comparing reinforcement learning algorithms.
Implementation of Q-Learning to learn optimal q-table of "Taxi-v3 Open AI Gym" and use it to solve the environment.

<p align="center">
<img src ="https://qph.fs.quoracdn.net/main-qimg-efa34695528d52dcd06c55d5d9b46bef-c" />
</p>

### Hyperparameters and optimizations
The values of `alpha`, `gamma`, and `epsilon` were mostly based on intuition and some "hit and trial", but there are better ways to come up with good values.

Ideally, all three should decrease over time because as the agent continues to learn, it actually builds up more resilient priors;

- α: (the learning rate) should decrease as you continue to gain a larger and larger knowledge base.
- γ: as you get closer and closer to the deadline, your preference for near-term reward should increase, as you won't be around long enough to get the long-term reward, which means your gamma should decrease.
- ϵ: as we develop our strategy, we have less need of exploration and more exploitation to get more utility from our policy, so as trials increase, epsilon should decrease.

### References
**[1]** *Sutton, R. S. & Barto, A. G.* [Reinforcement learning: an introduction](http://web.stanford.edu/class/psych209/Readings/SuttonBartoIPRLBook2ndEd.pdf), 1988.

**[2]** *T Erez, Y Tassa, E Todorov* [Hierarchical Reinforcement Learning with the MAXQ Value Function Decomposition](https://dl.acm.org/citation.cfm?id=1622268), 2011.
