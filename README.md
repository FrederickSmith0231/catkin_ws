# catkin_ws

Required directories are detection_msgs, gazebo_ros_link_attacher, gazebo_ros_pkgs, realsense-ros, robotiq, robotiq_gazebo, robotiq_urcap_control, ros_ur3, universal_robot, universal_robots_ros_drivers, ur_msgs, yolov5_ros. To install libraries please follow the readme's within there directory.

NB most of the directories needed have been copied and some have been edited. Origanal directories can be found on github.

Launch files required to:

rviz, arm with gripper roslaunch ur3_description display_with_gripper_85.launch ur_robot:=ur3 roslaunch ur_gripper_85_moveit_config start_moveit.launch rosrun ur_control moveit_tutorial.py --tutorial

rviz, arm with gripper and camera roslaunch ur3_description display_with_camera_435_and_gripper_85.launch ur_robot:=ur3 roslaunch ur_gripper_85_moveit_config start_moveit.launch rosrun ur_control moveit_tutorial.py --tutorial

gazebo, simulation of arm with cubes roslaunch ur3_gazebo ur_gripper_85_cubes.launch ur_robot:=ur3 grasp_plugin:=1 roslaunch ur_gripper_85_moveit_config start_moveit.launch rosrun ur_control moveit_tutorial.py --tutorial

gazebo, simulation of arm with a door roslaunch ur3_gazebo ur_gripper_85_door.launch ur_robot:=ur3 grasp_plugin:=1 roslaunch ur_gripper_85_moveit_config start_moveit.launch rosrun ur_control moveit_tutorial.py --tutorial

gazebo, simulation of depth camera roslaunch realsense2_description view_d435_model_rviz_gazebo.launch

gazebo, simulation of arm, gripper, camera and a door roslaunch ur3_gazebo ur_camera_gripper.launch

yolov5, object detection on image roslaunch yolov5_ros yolov5.launch
