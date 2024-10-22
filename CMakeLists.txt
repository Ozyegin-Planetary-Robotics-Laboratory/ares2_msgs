cmake_minimum_required(VERSION 3.5)
project(ares2_msgs)

# Find dependencies
find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)
find_package(std_msgs REQUIRED)
find_package(geometry_msgs REQUIRED)
find_package(sensor_msgs REQUIRED)

# Generate custom messages
rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/MotorCommand.msg"
  "msg/WheelCommandArray.msg"
  "msg/MotorFeedback.msg"
  DEPENDENCIES std_msgs geometry_msgs sensor_msgs
)

# Fix the installation path for generated headers
install(DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/rosidl_generator_cpp/ares2_msgs/msg/
  DESTINATION include/ares2_msgs/msg
)

ament_package()
