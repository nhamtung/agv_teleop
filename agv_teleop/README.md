# agv_teleop

# Install package
- Add command to install in CMakeLists.txt:
```
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
```
- Directory to workspace
- Build install: $catkin_make install
- Source: $source install/setup.bash
- Delete the src folder (delete source code)