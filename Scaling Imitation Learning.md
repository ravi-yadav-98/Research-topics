## Paper Title: SCALING IMITATION LEARNING IN MINECRAFT
--------------------------------------------------------------------
### Summary:
#### Keywords Definition
- *MineCraft* ---> Video Game (Most played)
- *Mine* *RL* --->  AI/Machine Learning for solving Minecraft game (Reinforment Learning techniques)
- *Imitation Learning* --> Imitation Learning is a framework for learning a behavior policy from demonstrations. 
    - Transfering human knowledge about the world to the RL agent
    - Learning from Demonstrations
    - The idea of Imitation Learning is implicitly giving an agent prior information about the world by mimicking human behavior in some sense

     
<br/>
- Approaches of Imitation Learning:
  > behavioural cloning
  > Direct Policy Learning
  > Inverse RL
<br/>
Challenges of RL:
-  Sparse Reward with time


### Training setup
- state and action space : 64x64 image
- ![image](https://user-images.githubusercontent.com/85448160/121345174-2c1c2a80-c942-11eb-94ff-30c481f7fb14.png)


- the policy neural network consists of three parts. A convolutional perceptual part for the image
input and a fully-connected part for the vectorial part of the state are concatenated after the last layer and followed by a
subseqent fully-connected part
- 


