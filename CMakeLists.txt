cmake_minimum_required(VERSION 3.0.2)
project(franka_msgs_archemist)

find_package(catkin REQUIRED COMPONENTS
  rospy
  std_msgs
  message_generation)

add_message_files(
   FILES
   PandaTask.msg
   TaskStatus.msg)

generate_messages(DEPENDENCIES std_msgs)


catkin_package(CATKIN_DEPENDS message_runtime)

include_directories(${catkin_INCLUDE_DIRS})