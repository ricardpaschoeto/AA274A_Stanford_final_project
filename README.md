# Autonomous Food Delivery

The final project will be based on Autonomous Food Delivery! You will be expected to (1) explore an unknown environment and locate all the food vendors around the city, then (2) given a food request from your hungry TAs, your robot will need to autonomously pick up the food and deliver it back to the home base.

![City](/pictures/city.png)

To summarize the robot moviment control, bellow we can see the Homeworks implemented along the course and working together to create the robot system control:

![Process](/pictures/robot.png)

The mainly Mission:

1.Explore
  * Navigate the city without colliding into obstacles
      * SLAM
      * Planning + Control
  * Record locations of food vendors
      * Object Detection
      * State Estimation
2.Deliver
  * Receive and process requests for delivery
      * ROS pub/sub
  * Autonomously drive through the city to pick up desired items and deliver them to the goal
      * Planning + Control

## Project Description

The robot control follows the Finite State Machine bellow:

![FSM](/pictures/FSM.png)

Besides the basic robot control - Explore the town to find different food vendors avoiding obstacles and pick up carry out orders for delivery - we implement extensions

## Installation

* Ubuntu 16.04 - https://ubuntu.com/download
* ROS Noetic   - http://wiki.ros.org/noetic/Installation/Ubuntu
* pyton2.7     - https://www.python.org/downloads/release/python-2716/

## Authors and acknowledgment

## Project status
