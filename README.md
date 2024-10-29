# Welcome to the third week of our Reinforcement Learning course! In this lab session, we challenge you to implement and extend what you've learned in the previous two weeks.

This graded lab may be more time-consuming and challenging, but it will be a rewarding experience as you tackle complex problems in reinforcement learning.

Educational Objectives
• Implement several RL algorithms for the Frozen Lake environment.
• Be able to extend the algorithm from Week 1 to the use a policy based on the current learning instead of random behaviour
• Implement the incremental version of the Monte Carlo algorithm.
• Be able to compare the performance of different RL methods.

Getting Started
Please group up in pairs. You will extend the notebooks we work with in the last two weeks.

Tasks
• This graded lab is designed for you to prove your understanding of the learned methods and apply them to the Frozen Lake Environment. The tasks are threefold:

1. Monte Carlo with a random policy: For the first task, you are required to implement the Monte Carlo algorithm from the first week's lab in the Frozen Lake environment, i.e. taking actions based on a random choice.
2. Incremental Monte Carlo: In the second task, extend the Monte Carlo algorithm from the first task to an incremental Monte Carlo method. See top equation in slide 30 from week 2. Incremental Monte Carlo updates the value estimates incrementally, reducing the need to wait until the end of an episode all episodes to update values. This should lead to more efficient learning. You should also incorporate a strategy to balance exploration and exploitation using ε-Greedy.
3. Q-Learning Integration: For the final task, you should replace the Monte Carlo method used and extended in the first two tasks with the Q-Learning algorithm, as introduced last week. This will allow you to compare the performance of Q-Learning with the Monte Carlo approach and observe how the learning process differs.

Note on Monte Carlo implementations
In the literature you can find two ways of implementing Monte Carlo (MC): First-Visit vs. Multiple-Visits MC. First-Visit MC only takes into account the return estimated from the first time a state is visited, while Multiple-Visits considers all visits to a given state.
Both methods are proven to converge to the optimal value function. In practical terms, some people suggest that in cases where sampling of the environment is costly, use of Multiple-Visits MC can be advisable.
A formal difference is that the First-Visit MC will yield truly independent samples of the return, which is not the case for the Multiple-Visits case. As a result, First-Visit MC provided an unbiased estimation in a similar way to maximum likelihood estimators. You can see more details about these methods in Section 5.1 of the Sutton’s book.
For this practice you can choose one type of implementation.

Submission
Your submission should include the code used to implement the methods, and a report including:
Choice of MC implementation (First-Visit / Multiple-Visits)
List of hyperparameters values chosen for each of the methods, as well as the approach you used to select them.
Plot the performance of the algorithms, including:
• Length of trajectories.
• Learning curves wrt to the number of episodes.
• Value function learned by each algorithm.
• For each method, answer the following questions:
• Is the agent able to estimate correctly the value-function?
• Is the agent able to learn the right policy?
• Change the size of the environment to 11x11 and compare the learning process
General discussion on the performance and implementation of each method (max 1 page).
The deadline for completing this graded lab is the start of the lab session in week 7 (Nov 1st, midnight). Make sure to include the names of both students of the team in your submission.
Key Takeaways
• Advanced Techniques: You will be applying advanced reinforcement learning techniques, including state value functions, incremental Monte Carlo, and Q-Learning.
• Efficient Learning: Incremental Monte Carlo and Learning are designed to make learning more efficient by updating value estimates incrementally.
• Comparative Analysis: By implementing different learning algorithms for the same environment, you will gain insights into the performance differences between the Monte Carlo method and Q-Learning in action.
