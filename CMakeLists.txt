cmake_minimum_required(VERSION 2.8.3)
project(blinky_bringup)

find_package(catkin REQUIRED COMPONENTS
  roslaunch
)

###################################
## catkin specific configuration ##
###################################
catkin_package()

#############
## Install ##
#############

install(DIRECTORY
  launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

#############
## Testing ##
#############
roslaunch_add_file_check(launch/blinky.launch)
