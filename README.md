
# Pirate Intelligent Agent

**CS-370: Current and Emerging Trends in Computer Science**  
**Ugljesa Stajic | Southern New Hampshire University**

## Project Overview

For Project Two in CS-370, I worked on a pirate intelligent agent that learns to navigate a maze and find treasure. Instead of programming a fixed path, the goal was to use deep Q-learning so the pirate could learn from its actions and the rewards it received. I completed the project in Python using a Jupyter Notebook and TensorFlow/Keras.

## What Code Was Provided, and What Did I Create?

The starter project included two Python classes and a partially completed notebook. `TreasureMaze.py` handled the maze environment, movement, rewards, and win/loss conditions. `GameExperience.py` handled experience replay, allowing the agent to learn from previous moves. The notebook already contained the maze setup, neural network, testing helpers, and a partially completed `qtrain()` function.

My main task was completing the training logic inside `qtrain()`. I added the steps for starting the pirate from random valid positions, choosing between exploring and using what it had learned, taking actions, and recording each experience. I connected the replay data to the model's training step, tracked the loss and win rate, updated the target network periodically, and checked whether the agent could consistently reach the treasure. I did not modify the provided Python classes.

In the saved training run, the agent reached a **100% win rate over its most recent 32 games at epoch 388** and passed the completion check from the eligible starting positions. That showed it learned to solve the provided maze, although it does not prove that every path was the shortest possible one.

## What Do Computer Scientists Do, and Why Does It Matter?

Computer scientists use algorithms, software, and data to solve problems. I think the job goes beyond writing code. It also involves understanding a problem, designing a solution, and testing whether that solution works as intended. Their work matters because software is part of almost everything we use, from business systems to transportation and robotics.

This project was a good example of that. Rather than telling the pirate exactly where to go, I worked with a system that could learn a useful strategy through experience. That is especially interesting to me because I am interested in AI and autonomous systems.

## How Do I Approach a Problem as a Computer Scientist?

I start by trying to understand the problem before changing the code. In this case, I reviewed how the maze, rewards, valid moves, and training functions worked together. Then I broke the task into smaller steps: selecting actions, recording experiences, training the network, and checking the results.

One thing I took away from this project is that I should not trust a single performance number. A good win rate during training is encouraging, but it does not automatically mean the agent can solve the maze from every starting point. Using the completion check helped me evaluate whether the solution was actually reliable.

## What Are My Ethical Responsibilities to the End User and the Organization?

I believe my responsibility is to create software that is reliable, secure, and honest about what it can and cannot do. That includes testing carefully, protecting user information, documenting important decisions, and thinking about what happens when a system makes a mistake.

Even though the pirate agent is only part of a game, the same concerns apply to real AI systems. A model might perform well during training but fail in situations it has not seen. As a developer, I should be transparent about those limitations and consider safety, fairness, privacy, and the effects of incorrect decisions before people rely on the system.

## Project Notebook

[`Stajic_Ugljesa_ProjectTwo.ipynb`](Stajic_Ugljesa_ProjectTwo.ipynb) contains the completed code and saved training output. The notebook does not store the trained model weights, so running it again requires retraining. It also needs the provided `TreasureMaze.py` and `GameExperience.py` files available in the Python environment.
