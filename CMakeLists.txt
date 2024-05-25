cmake_minimum_required(VERSION 2.8.3)
project(monogs)

set(CMAKE_BUILD_TYPE "Release")

# Find catkin and any dependencies declared in package.xml
find_package(catkin REQUIRED COMPONENTS
  std_msgs
  rospy
  roscpp
)

# Declare a catkin package
catkin_package(
  CATKIN_DEPENDS std_msgs rospy roscpp
)

# Include directories
include_directories(${catkin_INCLUDE_DIRS})

# catkin_python_setup()

catkin_install_python(PROGRAMS src/slam.py
                      DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})
