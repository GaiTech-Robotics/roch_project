roch
=====

Common ROS packages for the SawYer roch, useable for both simulation and
real robot operation.

 - roch_control : Control configuration
 - roch_description : Robot description (URDF)
 - roch_msgs : Message definitions
 - roch_navigation : Navigation configurations and demos

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
##### Source code installation

	Open one terminal and run:

	$ sudo apt-get install ros-indigo-robot-localization ros-indigo-interactive-marker-twist-server ros-indigo-twist-mux ros-indigo-joint-sate-controller ros-indigo-diff-drive-controller ros-indigo-imu-sensor-controller ros-indigo-realsense-camera ros-indigo-librealsense ros-indigo-realsense-camera ros-indigo-yocs-controllers ros-indigo-ecl-command-line ros-indigo-controller-manager ros-indigo-joy ros-indigo-ecl-threads libusb-dev libftdi-dev
  
  * ** Create your own workspace **
    * `$ cd && mkdir -p catkin_ws/src`
    * `$ cd catkin_ws/src`
  * ** Get source code from Github **
    * ` $ git clone https://github.com/SawYer-Robotics/roch_project.git`
    * ` $ git clone https://github.com/SawYer-Robotics/ls01c.git`
    * ` $ cd .. && catkin_make`
  * ** Install source code to system directory**
    * Because of ROS packages will use system environment variables so should follow under lines. And now you should under directory of `~/catkin_ws` then run this:
    * `$ sudo su` (type your password)
    * `$ source devel/setup.bash`
    * `$ catkin_make install -DCMAKE_INSTALL_PREFIX=/opt/ros/indigo`

Reopen terminal then run this command for check out:
  * ** Check out Roch env **
    * `$ env | grep ROCH_` (successfully when show values )