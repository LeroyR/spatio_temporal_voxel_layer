cmake_minimum_required(VERSION 2.8.3)
project(spatio_temporal_voxel_layer_msgs)

add_definitions (-std=c++17)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  message_generation
)

add_service_files(DIRECTORY srv
  FILES
  SaveGrid.srv
)

generate_messages(
   DEPENDENCIES
   std_msgs
)

catkin_package()
