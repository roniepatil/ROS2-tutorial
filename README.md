# ROS2 Tutorial

This repository contains a tutorial on how to install and set up ROS2, start your first ROS2 node, create and set up a ROS2 workspace, create a ROS2 python package, create a ROS2 node with python and OOP, write a ROS2 closed loop with publisher and subscriber, what is ROS2 Topic, what is ROS2 Publisher and subscriber, and how to write a ROS2 Service client with python.

## Table of Contents

- [Installation](#installation)
- [Getting Started](#getting-started)
- [ROS2 Workspace](#ros2-workspace)
- [ROS2 Python Package](#ros2-python-package)
- [ROS2 Node with Python and OOP](#ros2-node-with-python-and-oop)
- [ROS2 Closed Loop with Publisher and Subscriber](#ros2-closed-loop-with-publisher-and-subscriber)
- [ROS2 Topic](#ros2-topic)
- [ROS2 Publisher and Subscriber](#ros2-publisher-and-subscriber)
- [ROS2 Service Client with Python](#ros2-service-client-with-python)

## Installation

To install ROS 2 on your system, follow the instructions provided in the official documentation of ROS 2. You can find the installation guide at https://docs.ros.org/en/humble/Installation.html.

## Getting Started

After installing ROS 2 on your system, you can start your first ROS 2 node by following the instructions provided in the official documentation of ROS 2. You can find the tutorial at https://ubuntu.com/tutorials/getting-started-with-ros-2.

## ROS 2 Workspace

To create and set up a ROS 2 workspace, follow the instructions provided in the official documentation of ROS 2. You can find the tutorial at https://docs.ros.org/en/humble/Tutorials/Workspace/Creating-A-Workspace.html.

## ROS 2 Python Package

To create a ROS 2 python package, follow the instructions provided in the official documentation of ROS 2. You can find the tutorial at https://docs.ros.org/en/humble/Tutorials/Creating-Your-First-ROS2-Package.html.

## ROS 2 Node with Python and OOP

To create a ROS 2 node with python and OOP, follow the instructions provided in the official documentation of ROS 2. You can find the tutorial at https://docs.ros.org/en/humble/Tutorials/Writing-A-Simple-Py-Publisher-And-Subscriber.html.

## ROS 2 Closed Loop with Publisher and Subscriber

To write a ROS 2 closed loop with publisher and subscriber.

## ROS 2 Topic

A topic is a named bus over which nodes exchange messages.

## ROS 2 Publisher and Subscriber

A publisher is a node that sends messages on a topic while a subscriber is a node that receives messages from a topic.

## ROS 2 Service Client with Python

To write a ROS 2 service client with python


## EXTRA - Useful commands

export PATH="/usr/local/cuda-11.8/bin:$PATH"

export LD_LIBRARY_PATH="/usr/local/cuda-11.8/lib64:$LD_LIBRARY_PATH"

export PATH="/home/rohit/.local/bin:$PATH"

source /opt/ros/humble/setup.bash

source /usr/share/colcon_argcomplete/hook/colcon-argcomplete.bash

source ~/ros2_ws/install/setup.bash

mkdir ros2_wc

cd ros2_wc

mkdir src

colcon_build

source install/setup.bash

cd src

ros2 pkg create my_robot_controller --build-type ament_python --dependencies rclpy

cd ..

colcon build

[note: Current version installed - setuptools  59.6.0]

pip3 install setuptools==58.2.0

cd ~/ros2_ws/src/my_robot_controller/my_robot_controller 

touch my_first_node.py

chmod +x my_first_node.py

./my_first_node.py

#Below will prevent you to build every-time you change something in py files.

colcon build --symlink-install 

ros2 run my_robot_controller test_node

ros2 node list

ros2 node info /first_node

rqt_graph

ros2 topic list

ros2 topic info /chatter

ros2 interface show std_msgs/msg/String

ros2 topic echo /chatter

ros2 run turtlesim  turtlesim_node

ros2 run turtlesim turtle_teleop_key

ros2 run demo_nodes_cpp add_two_ints_server

ros2 service list

ros2 node list

ros2 service type /add_two_ints

ros2 interface show example_interfaces/srv/AddTwoInts

ros2 service call /add_two_ints example_interfaces/srv/AddTwoInts “{‘a’:2, ‘b’:5}”

ros2 run turtlesim turtlesim_node

ros2 run turtlesim turtle_teleop_key

ros2 service list

ros2 service type /turtle1/set_pen

ros2 interface show turtlesim/srv/SetPen

ros2 service call /turtle1/set_pen turtlesim/srv/SetPen “{‘r’:255, ‘g’:0, ‘b’:0, ‘width’:3, ‘off’: 0}”

ros2 topic hz /turtle1/pose
