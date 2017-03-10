# roch_project
Roch robot of SuZhou SawYer robotics

## Instructions
This project have not use anymore, and divided into four repositories showing fowllow.

### Roch
Roch repository contains all apps for Roch, with [roch code](http://github.com/SawYer-Robotics/roch) and [wiki](http://wiki.ros.org/roch)

### Roch_robot
Roch_robot repository includes all drivers and communication with [Roch](http://wiki.ros.org/Robots/Roch), with [roch_robot code](http://github.com/SawYer-Robotics/roch_robot) and [wiki](http://wiki.ros.org/roch_robot)

### Roch_simulator
Roch_simulator repository provides simulator with Roch without real machine, which for now just support Gazebo, with [roch_simulator code](http://github.com/SawYer-Robotics/roch_simulator) and [wiki](http://wiki.ros.org/roch_simulator)

### Roch_viz
Roch_viz repository just provides visualization tools when using Roch, with [roch_viz code](http://github.com/SawYer-Robotics/roch_viz) and [wiki](http://wiki.ros.org/roch_viz)

## Installation Guide

## Preparation

This project is ROS packages for Roch, so before you begin should follow thess steps for preparation with depend on some packages that Roch ROS packages must have to run. 

Requirements under these lines 

Name  | Requierment  |
----- | ------------ |
3D Sensors USB   | USB3.0 |
Ubuntu | 14.04 |
Kernel | v4.4-wily and above |
GCC | 4.9 |

And requierment of kernel just for Realsense 200, follow this for [update Ubuntu kernel](https://github.com/IntelRealSense/librealsense/blob/master/doc/installation.md)

### Source code installation

Open one terminal and run:

	$ sudo apt-get install ros-indigo-robot-localization ros-indigo-interactive-marker-twist-server ros-indigo-twist-mux ros-indigo-joint-sate-controller ros-indigo-diff-drive-controller ros-indigo-imu-sensor-controller ros-indigo-realsense-camera ros-indigo-librealsense ros-indigo-realsense-camera ros-indigo-yocs-controllers ros-indigo-ecl-command-line ros-indigo-controller-manager ros-indigo-joy ros-indigo-ecl-threads libusb-dev libftdi-dev
  
  * **Create your own workspace**
    * `$ cd && mkdir -p catkin_ws/src`
    * `$ cd catkin_ws/src`
  * **Get source code from Github**
    * ` $ git clone https://github.com/SawYer-Robotics/roch_project.git`
    * ` $ git clone https://github.com/SawYer-Robotics/ls01c.git`
    * ` $ cd .. && catkin_make`
  * **Install source code to system directory**
    * Because of ROS packages will use system environment variables so should follow under lines. And now you should under directory of `~/catkin_ws` then run this:
    * `$ sudo su` (type your password)
    * `$ source devel/setup.bash`
    * `$ catkin_make install -DCMAKE_INSTALL_PREFIX=/opt/ros/indigo`

Reopen terminal then run this command for check out:
  * **Check out Roch env**
    * `$ env | grep ROCH_` (successfully when show values )
