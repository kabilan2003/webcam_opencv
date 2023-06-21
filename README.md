# webcam_opencv interfacing 

How to Install a USB Camera in diffential robot 

# Installing ROS OpenCV camera driver


sudo apt update 

sudo apt install ros-noetic-cv-camera

# Once you have this installed in your raspberry pi, you can plug it in a USB port and test it running this node:

source /opt/ros/noetic/setup.bash

rosrun cv_camera cv_camera_node

# it wil publish image_raw and some more topics 

Type rostopic list in terminal

# If it works, then create a launch file for the node and also a static transform publisher from base_link to camera_link



<launch>
  <node pkg="cv_camera" type="cv_camera_node" name="cv_camera" output="screen"/>
  <node pkg="tf" type="static_transform_publisher" name="camera_frames_pub" args="0.05 0.0 0.1 0 0 0 /base_link /camera 35"/>
</launch>

# Youtube video
https://youtu.be/A3CTi3QnZZ0!

# Raspberry pi robot with webcam

[20230621_145156](https://github.com/kabilan2003/webcam_opencv/assets/109456728/35977759-cae1-4803-b86d-4cc7296bb10f)

