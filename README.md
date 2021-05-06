# MiniRos: an autonomous UGV robot for educationand research

MiniRos is a small autonomous UGV-Unmanned ground vehicle developed for education and research purposes. Its small payload capacity and power system are suitable for various types of loads, customized to meet research needs. In this paper, we develop MiniRos with a compact structure and high torque drive system that can take research to the outdoor environment. MiniRos is run on a Robot Operating System (ROS), which has been developed to be compatible with standard robotics programming environments. MiniRos sense the environment with a depth camera Intel Realsense D435, Hokuyo 2D Lidar scanner URG-04LX and performs all processing onboard with Jetson Nano. MiniRos can build 2D map with SLAM algorithms, avoiding obstacles, localize within a global map, navigation in the built map. Moreover, MiniRos simulation on Gazebo environment is available as open-source, this is a useful tool for researchers and educators.

![MiniROS 3D design](https://github.com/TriKnight/miniros/blob/master/figures/minibot_3.png)

## Installation

Step 1. Install Ubuntu 18.04 and  [ROS Melodic!](http://wiki.ros.org/melodic/Installation/Ubuntu)

Step 2. Following [ROS Tutorial](http://wiki.ros.org/ROS/Tutorials) and create **catkin_ws**

Step 3. Git clone Miniros and some repos:

```
cd ~/catkin_ws/src
git clone https://github.com/TriKnight/miniros/
git clone https://github.com/ros-teleop/teleop_twist_keyboard
```

Step 4. Install all ROS dependences

```
cd ~/catkin_ws
rosdep install --from-paths src --ignore-src -r -y
catkin_make
```
Step 5. Running Miniros empty world gazebo enviroments 

```
roslaunch miniros_gazebo minibot_world.launch
```
![Minibot in world](https://github.com/TriKnight/miniros/blob/master/figures/Screen%20Shot%202021-05-06%20at%2010.45.39%20PM.png)


