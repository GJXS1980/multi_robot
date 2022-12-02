# Multiple TurtleBot3 Navigation Environment
Literally as title, this package provides launch files allowing turtlebots to navigate in "the house". 


## Installation
1. Install ROS. (Hey Google, what is ROS?)
2. Clone all relative packages into <your_ws>/src/.
```
source /opt/ros/melodic/setup.bash
cd catkin_ws/src
git clone https://github.com/GJXS1980/multi_robot.git
cd .. && catkin_make
source devel/setup.bash
```

## Usage 
1. First terminal -- Launch the simulation

* Launch multiple turtlebot3 in Gazebo simulation.
```
roslaunch turtlebot3_gazebo multi_turtlebot3.launch
```

2. Second terminal -- Launch navigation stacks

* Launch Navigation for three turtlebot3.
```
roslaunch turtlebot3_navigation multi_nav_bringup.launch
```

## Control with Behavior Tree
```
rosrun bt_sample node _file:=/home/<user>/catkin_ws/src/BT_ros1/BT_sample/cfg/multi_bt.xml
```
The behavior tree will set goal to each robot. [See the DEMO](https://www.youtube.com/watch?v=hilXQiEUrk8)
