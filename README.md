# Autonomous Food Delivery

The final project will be based on Autonomous Food Delivery! You will be expected to (1) explore an unknown environment and locate all the food vendors around the city, then (2) given a food request from your hungry TAs, your robot will need to autonomously pick up the food and deliver it back to the home base.

![City](/pictures/city.png)

To summarize the robot moviment control, bellow we can see the Homeworks implemented along the course and working together to create the robot system control:

![Process](/pictures/robot.png)

The Mission Outline:

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

The robot will navigate on the map and searching for three vendors – Broccoli, Pizza, Hot-Dog. We can operate the robot manually or set a list containing vendors' sequence to visit sequentially; for this, we worked on the A* algorithm to solve multiple sequential paths. Bellow we show up the A* Algorithm exaples:

![AStar01](/pictures/a_star01.png)              ![AStar01](/pictures/a_star02.png)

The Baseline for the project is listed bellow:

* Human operated waypoint following for exploration.
* Logging food locations through TF frames / broadcasting on a topic.
* Autonomous navigation to revisit vendors and drive to delivery location without running into fences.

The robot control follows the Finite State Machine bellow:

![FSM](/pictures/FSM.png)

Beyond of the baseline, we implement extensions:

 * Stop at stop signals
  The world will have at least three stop signs. When the robot comes to a stop sign, it will stop for five seconds and then continue on its planned path. 
 * Plan an optimal path
  The robot will plan the shortest time route between multiple vendors, accounting for the time to stop at stop signs.
 * Recognize a Dog 
  The robot will be on the lookout for Dog around the world and doing something fun.

## Installation

* Ubuntu 16.04 - https://ubuntu.com/download
* ROS Noetic   - http://wiki.ros.org/noetic/Installation/Ubuntu
* pyton2.7     - https://www.python.org/downloads/release/python-2716/
* Rviz         - http://wiki.ros.org/rviz

## Authors and acknowledgment

This project was built by: Mason Murray-Cooper, Brice Pridgen, Toktam Mohammadnejad, Ricardo Luiz Moreira Paschoeto. The project was the result of the graduate course "Principles of Robot Autonomy I" from Stanford University. 

## Project status

For suggestions to advance the robot behavior some extension can be added:

* A filter that uses the pointcloud to track an object moving around the turtlebot
* Identifies a "puddle" on the ground and moves around it
* Provide an accurate distance estimate of a detected object using pointcloud data
* Accurate position estimate of detected objects
* Improve upon any of the existing asl turtlebot functionality
* Implement a fancy cool algorithm you heard about
