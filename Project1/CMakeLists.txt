cmake_minimum_required(VERSION 3.0 FATAL_ERROR)

find_package(gazebo REQUIRED)

include_directories(${GAZEBO_INCLUDE_DIRS})
link_directories(${GAZEBO_LIBRARY_DIRS})

add_library(welcome_message SHARED script/welcome_message.cpp)
target_link_libraries(welcome_message ${GAZEBO_LIBRARIES}
