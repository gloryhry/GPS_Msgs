cmake_minimum_required(VERSION 2.8.3)
project(gps_msgs)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  nav_msgs
  geometry_msgs
  message_generation
)

add_message_files(
  DIRECTORY msg
  FILES
  Novatelstatus.msg
  Posangle.msg
  gpstest.msg
  odomtest.msg
  twisttest.msg
  posetest.msg
  )

generate_messages(
  DEPENDENCIES
  std_msgs
  nav_msgs
  geometry_msgs
)

catkin_package(
  CATKIN_DEPENDS
  message_runtime
  std_msgs
  nav_msgs
  geometry_msgs
)
