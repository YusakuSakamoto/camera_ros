cmake_minimum_required(VERSION 2.8.3)
project(confirm_version)

## Find catkin and any catkin packages
find_package(catkin REQUIRED COMPONENTS roscpp rospy std_msgs genmsg OpenCV)

## Declare ROS messages and services

## Generate added messages and services

## Declare a catkin package
catkin_package()

## Build talker and listener
include_directories(include ${catkin_INCLUDE_DIRS})

add_executable(confirm_version src/main.cpp)
target_link_libraries(confirm_version ${catkin_LIBRARIES})
add_dependencies(confirm_version ${OpenCV_LIBS})
