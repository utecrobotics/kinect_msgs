cmake_minimum_required(VERSION 2.8.3)
project(kinect_msgs)

find_package(catkin REQUIRED COMPONENTS
  genmsg
  geometry_msgs
  std_msgs
  roscpp
  rospy
)

add_message_files(
   FILES
   BodyArray.msg
)

generate_messages(
   DEPENDENCIES
   geometry_msgs
   std_msgs
 )

catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
)

