---
title: "BAXTER BUILDS TOWERS WITH CUPS"
excerpt: "Rethink Robotics' Baxter sorts and builds towers with plastic cups.<br/><img src='/images/fasttower.gif'>"
collection: portfolio
---


# Project Overview
This is a ROS project developed as part of ME495 - Embedded Systems in Robotics course at Northwestern University.

The goal of this project is to use the BAXTER robot and build a "HUGE" tower from plastic cups

You can find the Github repository at the following link: 

https://github.com/rubberdk/final-project-fast-tower

# Demonstration

10 Cups Tower <br/>
[![1](http://img.youtube.com/vi/YzLpgf8ozkA/0.jpg)](http://www.youtube.com/watch?v=YzLpgf8ozkA)

6 Cups Tower <br/>
[![2](http://img.youtube.com/vi/H2U9Fk785CE/0.jpg)](http://www.youtube.com/watch?v=H2U9Fk785CE)

6 Cups sorting <br/>
[![3](http://img.youtube.com/vi/yFVovQYhw8g/0.jpg)](http://www.youtube.com/watch?v=yFVovQYhw8g)

# Project Details

## Gazebo Simulation
![](https://raw.github.com/rubberdk/rubberdk.github.io/master/images/baxter_gazebo.png)<br/>

- Baxter Simulator
- Tool utilized to test code without real robot
- Get the position of the cups with get_model_state service
- Set cup pose with set_model_state

## Rviz
![](https://raw.github.com/rubberdk/rubberdk.github.io/master/images/baxter_rviz.png)<br/>

- Moveit to set the planning Scene and Rviz visualizer
- To set the positions of the cups and tables
- To add the objects to the scene 
- To return information about the scene


## Robot Control
![](https://raw.github.com/rubberdk/rubberdk.github.io/master/images/baxter_control.png)<br/>
Let one hand first place what it’s grabbing, then let the other hand grab the next cup to place.
 
## Computer Vision
![](https://raw.github.com/rubberdk/rubberdk.github.io/master/images/baxter_cv.png)<br/>
![](https://raw.github.com/rubberdk/rubberdk.github.io/master/images/baxter_cvr.png)<br/>

- We used a aprtiltag_ros which is a ROS wrapper of the AprilTag to get x,y,z positions of the cups.
- We mainly used the Baxter's right hand camera for tag deteection,but we gave options to use left camera or the head camera.
- Then simulator.py which is a MoveIt Python API coverts tf data to x,y,z positions and add positions and visual cylinders that represent cups to the scene that can be seen in Rviz
- Arm_control nodes use those positions for Baxter's task for sorting or building cups


# Project Team Members

Dimitrios Chamzas

Dong Ho Kang

Yuxiao Lai

Gabrielle Wink
