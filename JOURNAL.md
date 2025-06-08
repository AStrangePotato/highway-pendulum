---
title: Double Pendulum Balancer
author: "Daniel Zhang"
description: "A physical model of a double pendulum that can be controlled by a reinforcement learning agent."
created_at: "2025-06-05"
---


### June 5: research into cartpole!
The main motivation for this project comes from wanting to bring RL into the physical world. I've trained in simulations before, but I want to build a desktop model.

Did a lot of research into parts, how motors work, stepper vs servo vs brushless (still a bit confused, this is my first real hardware project.)

Belt system to move cart (probably some kind of stepper motor with a rail?)

Pendulum system (probably going to start with single pendulum for training)

Want to recreate something like this. ![image](https://github.com/user-attachments/assets/5ce6fd69-1008-45c2-aaab-156578da629d)

**Time: 1hr**


### June 8: Part selection

I didn't really understand motors before, but now I learned theres servos, DC's, and steppers. A stepper motor seemed good for this kind of project, and I also ordered a driver to go with it, as well as a set of ball bearings for the pendulum. I did some more research into how I'm going to connect my PC to train the agent to the physical simulation, and I think I will use a webcam to track the links of the pendulum, and calcualte the required data.

Inputs to agent:
- sin and cos of theta1 (of base joint)
- sin and cos of theta2 (of secondary joint)
- angular velocites

The interesting reason behind using sin of the angle is to map the angle to a smooth continuous function, rather than it skiping (say 0 to 360), which is bad for the agent learning. The reason behind using both is so that there is no ambiguity (sine law case!)

I've decided to go with something simpler instead of the cart pole because I think I know where my skill is at, and doing an easier project will be just as rewarding. I will extend my physical RL experience to harder projects in the future.

**Total time: 1 + 1 = 2 hrs**

