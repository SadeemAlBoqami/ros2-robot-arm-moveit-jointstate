# ros2-robot-arm-moveit-jointstate
Controlling the robot arm by 2 methods:  

1-  joint_state_publisher.  
2- Moveit and kinematics

## Project Overview: 
This project demonstrates controlling a robotic arm using ROS 2. It supports two main control methods:  

1. **Joint State Publisher** – for manual joint manipulation and basic visualization in RViz.
2. **MoveIt + Kinematics** – for motion planning and executing pre-defined or dynamically generated trajectories.
   
The goal is to showcase how both low-level and high-level control methods can be implemented within the ROS 2 ecosystem. The project is useful for learning robot kinematics, MoveIt integration, and visualization using RViz2 and Gazebo.

## Requirements:
- Ubuntu 22.04 or compatible.
- ROS2 (e.g. Humble).
- [Robot_Arm_ROS2 Package](https://github.com/Mjd0001/Robot_Arm_ROS2) Make sure to clone and install the original package by following the instructions in its repository:
    - [Dependencies](https://github.com/Mjd0001/Robot_Arm_ROS2?tab=readme-ov-file#dependencies)
    - [Installation](https://github.com/Mjd0001/Robot_Arm_ROS2?tab=readme-ov-file#installation)
 

## Simulation and Usage:

### 1- Joint State Publisher
This method allows manual control of the robot arm joints through the GUI.

**Steps:**
1. Launch the robot description with joint state GUI:
from terminal: 
   ```bash
   $ ros2 launch arduinobot_description display.launch.py
   ```
2. Use the sliders in the GUI to move each joint.
3. Visualize the motion in RViz.

<img width="1600" height="900" alt="joint state sim" src="https://github.com/user-attachments/assets/e4dd394d-7c3b-4d1a-809f-eb76d19e6794" />



### 2- MoveIt + Kinematics
This method uses MoveIt for motion planning and inverse kinematics.

**Steps:**
1. Launch MoveIt with the robot arm:
```bash
ros2 launch  arduinobot_mc demo.launch.py
```
Another RViz window will open. Select `Approx IK Solutions` option and press the `Plan` command. You can move the arm using the ball.

<img width="1220" height="914" alt="moveit planning" src="https://github.com/user-attachments/assets/638a5499-cff7-48e7-b5db-5ef44521f544" />

