cmake_minimum_required(VERSION 3.8)
project(ros2_subscriber)

find_package(ament_cmake REQUIRED)
find_package(rclcpp REQUIRED)
find_package(std_msgs REQUIRED)

add_executable(subscriber_node src/subscriber_node.cpp)

ament_target_dependencies(subscriber_node
  rclcpp
  std_msgs
)

install(TARGETS
  subscriber_node
  DESTINATION lib/${PROJECT_NAME}
)

ament_package()

