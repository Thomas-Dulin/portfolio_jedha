# Reinforcement learning - Training an artificial intelligence (AI) to play a video game

## Overview and objectives

This is the **final project** I did during my FullStack training at **Jedha**, together with my classmate Chunyan Frey. We presented this project during a **Youtube live**, whose replay is available [here](https://www.youtube.com/watch?v=XefhnowWji4&t=8210s), if you wanted to have a look at it (the presentation is in French).

The idea was simple but ambitious: to **train an artificial intelligence (AI) to play a video game**, in this case **Activision Tennis**, released in 1980 on the Atari 2600 console.

To do this, it was necessary to explore one of the sub-branches of machine learning: **reinforcement learning**.

## What is reinforcement learning?

Reinforcement learning appeared in the **1990s** and has since been popularised by projects run by organisations such as **DeepMind** or **OpenAI**. It aims to **simulate a learning process for an AI that is similar to that of a child**.

A **young child** has little knowledge of the world around her/him. To interact with the latter, s/he will therefore **undertake actions that are initially random**. Little by little, the responses transmitted to her/him by her/his environment (through her/his parents, for example) will enable her/him to **adapt her/his actions to make them more relevant**.

Let's take an example: a child who is given a spoonful of yoghurt in his hand does not instinctively know what to do with it. It is only because her/his parents guide her/him by encouraging or correcting her/him that s/he finally manages to use it properly. 

**Reinforcement learning copies this logic and applies it to artificial intelligence**. The idea is to create an **agent** (an artificial intelligence entity) and to confront it with a game, giving it only the **rules** (possible actions, for example). Regularly, **rewards (or punishments)** will be given to the agent, allowing it to **gradually learn to play**. The agent becomes **stronger with each iteration**, and after a while its level becomes similar (or even higher) than that of a human.

In short, like humans playing a video game (at least in theory!), it **learns from its mistakes**.

## Adaptability

For this project we used the **Gym** module developed by **OpenAI**, which allowed us to **simulate the Activision Tennis game environment**. This game is only one of the many games available through this library (more details [here](https://gym.openai.com/)). Feel free to try to adapt this code for other games!

This is what we did ourselves: our code is **largely inspired by [this project](https://github.com/gameofdimension/policy-gradient-pong)**, which was done on the game Pong.

## Files

Since AI agents learn from their own mistakes, there is **no dataset** in reinforcement learning!

The **notebook** in this folder should be sufficient on its own. However, it is very important to make one thing clear: **the code it contains is functional, but the results of the agent's training are still uncertain**.

Indeed, one of the particularities of reinforcement learning is the **considerable time required for training**. The latter is not counted in hours but in **days**... The exact time is not defined in advance, but to give you an idea, the code on which we based our training process only showed good performance after 90 hours, or 4 days! Knowing that our game is slightly more complex, one can imagine that the training would take **about a week**.

This is one of the main limitations of this field: while the code itself is not extremely complicated, it requires **powerful computing capabilities** to run (at least to be able to achieve satisfactory results).

**We have not yet been able to run this notebook for such a long time, so the potential results are completely uncertain**. This long training is the only thing that can attest to the validity of the code.

If you ever want to run this code yourself, it is certainly possible to use a computer alone, but solutions such as those offered by **Amazon** (SageMaker) or **Google** (Cloud Platform) seem particularly suitable. In this case, you may need to convert the notebook into a **Python script**.

The **checkpoints** set up in the notebook can also allow the training to be done in several times!

## Required libraries

This project uses six libraries: **NumPy** (data manipulation), **TensorFlow** (data manipulation and deep learning), **Gym** (video game environments), **time** (time access), **Matplotlib** (data visualization) and **os** (operating system interfaces).

Depending on your execution environment, you might need to **install these modules**. You can do so using a `pip install name_of_the_library` command. Remember to add an exclamation mark at the beginning if you want to execute it directly in a notebook, as it is originally a terminal command.