
# ares2_msgs

## Description
This package contains the custom message types used by the ares2_control package. These messages are essential for communication between various nodes in the ares2_control system.

## Prerequisites

Make sure you have the following dependencies installed:

- **ROS 2 Humble** (or a compatible version)
- **ament_cmake**: ROS 2 build tool
- **rclcpp**: ROS 2 C++ client library

## Build Instructions

1. Clone the repository:

   ```bash
   cd ~/ros2_ws/src
   git clone https://github.com/Ozyegin-Planetary-Robotics-Laboratory/ares2_msgs

2. Go back to the root of your workspace:

   ```bash
   cd ~/ros2_ws
   ```

3. Build the package:

   ```bash
   colcon build --packages-select ares2_msgs
   ```

## How to Run

Since this is a message package, it doesn't have executables to run directly. It is used as a dependency in other ROS 2 packages like `ares2_control`. Ensure that it is built and sourced before running the ares2_control nodes.

```bash
source ~/ros2_ws/install/setup.bash
```

This ensures that the custom messages in `ares2_msgs` can be found by any dependent packages.

## In the Future

Make sure to add messages to your projects from this directory in the right from such as:

```cpp
   #include "ares2_msgs/msg/motor_command.hpp"
   #include "ares2_msgs/msg/wheel_command_array.hpp"
   #include "ares2_msgs/msg/motor_feedback.hpp"
   ```


