
summit_sim
==========

Packages for the simulation of the Summit robot

<h2>summit_control</h2>

New gazebo 1.9 style robot control

<h2>summit_description</h2>

robot description (urdf and meshes).

<h2>summit_gazebo</h2>

launch files and world files to start the models in gazebo

<h2>summit_joystick_teleop</h2>

<p>node to process the joystick in simulation (configured for PS3, but others are also possible).</p>

<h2>summit_robot_control</h2>

<p>control the robot joints in all kinematic configurations, publishes odom topic and, if configured, also tf odom to base_link. Usually takes as input joystick commands and generates as outputs references for the gazebo controllers defined in summit_control.</p>

<h2>summit_purepursuit</h2>

<p>specific launch files to use the robotnik_purepursuit_planner to control the Summit passing waypoints in Cartesian coords<p>

Installation process (WIP)
====================
Intallation process for ROS-melodic

<h2>Prerequisites</h2>

- https://github.com/RobotnikAutomation/robotnik_purepursuit_planner
- https://github.com/RobotnikAutomation/robotnik_msgs
- https://github.com/ros-drivers/ackermann_msgs

Download this repository and checkout to "melodic" branch.

Execute Catkin_make in the catkin workspace.

If gazebo does show the following error:
```
[Err] [REST.cc:205] Error in REST request
libcurl: (51) SSL: no alternative certificate subject name matches target host name 'api.ignitionfuel.org'
```
The solution is to apply the change proposed in:
https://bitbucket.org/osrf/gazebo/issues/2607/error-restcc-205-during-startup-gazebo
