# 4wd robot vehicle (ros-bot)
## Introduction
This project is a ROS robot platform for autonomous navigation R&D. It was created as a proof of concept to use ROS for IUT's mars rover team. ROS(Robot Operating System) is the most popular platform for robotics which has many standard libraries for navigation, inverse kinematics etc. with documentations and community support.

## Implementation

This bot is basically an advanced version of [rc-soccerbot](https://github.com/RakinRkz/rc-soccerbot), which can be controlled via bluetooth or hobby transmitter reciever systems. It drives as a skid steering system. The underlying hardwares are:

  - Motors, Dual channel motor driver
  - Arduino uno
  - Raspberry pi 4b
    
The arduino is connected to the Raspberry pi via usb cable and it uses the ros-serial library. The arduino is set up as a ROS node which recieves command velocity(linear and angular) from the upper layer controller program running on the Raspberry pi. It then converts the command to motor control signals. PID tuning is required here for proper motor behavior. In the upper layer, the program sending command velocity can be a manual controller which has a GUI or an autonomous/semi-autonomous node that generates commands continuously.

## Conclusion
After successful implementation of this POC project, ROS was implemented on IUT mars rover team's rover and further improvement was carried on.
