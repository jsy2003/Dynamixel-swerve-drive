# ROS based independent steering and drive implementation with Dynamixel
## Overview
![38178150-674cf18e-3647-11e8-900b-5a8d76f3ddaa](https://user-images.githubusercontent.com/93853610/144552315-dca28a1a-784a-4c33-aea4-f5f2d97bb826.png)



## 1. Wiring & motor configure

   Motor's ID should be set as described picture below.
   You can set motor ID via [dynamixel_workbench](https://github.com/ROBOTIS-GIT/dynamixel-workbench/
   )(linux) or [R+ Manger 2.0](https://emanual.robotis.com/docs/en/software/rplus2/manager/)(windows)

   ![38525760-75d6b8dc-3c8e-11e8-80f0-17de58b6ce12](https://user-images.githubusercontent.com/93853610/144548403-636f2fdb-3a47-429a-aaa3-f3cba4e6e43f.png)


## 2.Prerequisites
   
   ### Follow packages should be installed
   ```
   $sudo apt-get install ros-noetic-dynamixel-sdk
   $sudo apt-get install ros-noetic-qt-build
   $sudo apt-get install ros-noetic-dynamixel-workbench
   $sudo apt-get install ros-noetic-dynamixel-workbench-msgs
   ```    

### 3. Download & compile the source
   1. Clone this reposiory to your catkin workspace
   ```
   $ cd catkin_ws/src
   $ git clone https://github.com/jsy2003/Dynamixel-swerve-drive.git
   ```
   2. Compile the source
   ```
   $ cd ~/catkin_ws
   $ catkin_make
   $ source devel/setup.bash
   ```
   3. Launch the swerve_drive_control node
   ```
   $ roslaunch swerve_drive swerve_drive_control.launch
   ```
   4. Open the new ternimal and start teleop_twist_keyboard script
   ```
   $ rosrun teleop_twist_keyboard teleop_twist_keyboard.py
   ```
   5. Control with twist keyboard command:
   - 'i'= forward
   - ',' = backward
   - 'j' = left turn
   - 'l' \ right turn
   6. (optional) To visualize swerve_drive in Rviz, open the new terminal
   ```
   $ roslaunch swerve_drive swerve_drive_urdf.launch
   ```
   
   
   
   
   
   

