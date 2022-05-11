cmake_minimum_required(VERSION 3.0.2)
project(agv_teleop)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES agv_teleop
#  CATKIN_DEPENDS roscpp rospy std_msgs
#  DEPENDS system_lib
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

#############
## Install ##
#############

## Mark executable scripts (Python etc.) for installation
catkin_install_python(PROGRAMS
  scripts/agv_teleop_key.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}/scripts
)
## Mark executables for installation
#install(TARGETS 
#  RUNTIME DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
#)
## Mark libraries for installation
#install(TARGETS ${PROJECT_NAME}
#  ARCHIVE DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION}
#  LIBRARY DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION}
#  RUNTIME DESTINATION ${CATKIN_GLOBAL_BIN_DESTINATION}
#)
## Mark cpp header, launch files for installation
#install(DIRECTORY include/${PROJECT_NAME}/
#  DESTINATION ${CATKIN_PACKAGE_INCLUDE_DESTINATION}
#  PATTERN ".svn" EXCLUDE
#)
install(DIRECTORY launch/
  DESTINATION ${CATKIN_PACKAGE_INCLUDE_DESTINATION}/launch
  PATTERN ".svn" EXCLUDE
)