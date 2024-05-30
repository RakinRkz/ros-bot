

## Pre requisites 

```
sudo apt install python-catkin-tools

sudo apt install ros-melodic-depthimage-to-laserscan
```
This repo contains everything. So no need to git clone depthimage-to-laserscan. Just 
catkin_make will work in noetic.







Please set the correct serial numbers of both the Realsense cameras

Use the following command to see the serial number of your cameras

***This is required for using multiple Realsense cameras***

```
rs-enumerate-devices

```


edit the contents of **realsensecameras.launch** with the proper serial numbers of the individual Cameras .


Catkin build , source the workspace and then you should be good to go !





For start-

roslaunch occupancy occupancy_live_rviz.launch
roslaunch jackal_navigation odom_navigation_demo.launch
