cmake_minimum_required(VERSION 2.8 FATAL_ERROR)
project(beginner_tutorials)
find_package(gazebo REQUIRED)

include_directories(${GAZEBO_INCLUDE_DIRS})
link_directories(${GAZEBO_LIBRARY_DIRS})
list(APPEND CMAKE_CXX_FLAGS "${GAZEBO_CXX_FLAGS}")

add_executable(listener listener.cc)
target_link_libraries(listener ${GAZEBO_LIBRARIES} pthread)

add_executable(listenerprueba listener_prueba.cc)
target_link_libraries(listenerprueba ${GAZEBO_LIBRARIES} pthread)





