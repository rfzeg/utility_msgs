# The utility_msgs respository

Author: Roberto Zegers  
Date: February 2023

## Description

This repository contains a collection of generic ROS message, service and action definitions.  

## Usage

- Clone to your ROS workspace, for instance into `~/catkin_ws/src`  
- Compile and source: `cd ~/catkin_ws; catkin_make; source devel/setup.bash` 

For any other package to use one of these generic definitions, the `CMakeLists.txt` must be modified by adding the following:  

```
find_package(catkin REQUIRED COMPONENTS
  utility_msgs                
  actionlib
  ...
)
...
catkin_package(
  CATKIN_DEPENDS utility_msgs ...
)
```
Additionally update the `<depend>` tags inside the `package.xml` file accordingly:  
```
<depend>utility_msgs</depend>
```

## Manual testing

```
rosmsg list | grep GenericFloatGoal
```

## License
- BSD-3-Clause  

## Dependencies
- ROS Noetic