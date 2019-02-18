# ROS openni 2.0 wrapper for LIPSedge DL/M3 ToF cameras #

### 1. Install the pre-required packages ###

* For Ubuntu 16.04 with ROS Kinetic
```
$ sudo apt-get install ros-kinetic-rgbd-launch
```
* For Ubuntu 14.04 with ROS Indigo
```
$ sudo apt-get install ros-indigo-rgbd-launch
```
### 2. Install openni2 package for Ubuntu ###
make sure you have openni2 package installed
```
$ sudo apt-get install libopenni2-0 libopenni2-dev
```
### 3. Download and install LIPS SDK with ROS support ###
Download .deb package from [LIPS SDK](https://www.lips-hci.com/downloads/category)
* Select your system: Ubuntu 14.04/16.04 (currently only support 64bit)
* Select the Platform: OpenNI2.2
```
$ sudo dpkg -i ROS-libmodule-lips2_1.5.0.7_arm64.deb
```
### 4. Download this openni 2.0 wrapper ###
This wrapper is modified to support resolution QQQVGA (80x60@30Hz).
```
$ mkdir -p ~/LIPSToF_ws/src
$ cd ~/LIPSToF_ws/src
$ catkin_init_workspace
$ git clone https://github.com/lips-hci/openni2_camera
```
### 5. Build and launch services ###
```
$ cd ~/LIPSToF_ws
$ ln -s src/openni2_camera/run.sh .
$ ln -s src/openni2_camera/view.sh .
$ ./run.sh
```
### 6. Launch viewer to check depth/ir images ###
Make sure LIPSedge ToF camera is already connected to your host PC.
```
$ ./view.sh
```
