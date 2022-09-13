cmake_minimum_required(VERSION 3.0.2)
project(camera_apps_msgs)

find_package(catkin REQUIRED COMPONENTS
    roscpp
    rospy
    std_msgs
    sensor_msgs
    geometry_msgs
    message_generation
    )

add_message_files(
  FILES
  BoundingBox.msg
  BoundingBoxes.msg
  ObjectState.msg
  ObjectStates.msg
  ObjectInfo.msg
  ObjectsInfo.msg
  Mask.msg
  Masks.msg
)


## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs  # Or other packages containing msgs
  geometry_msgs
  sensor_msgs
  # OpenCV
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES camera_apps_msgs
    CATKIN_DEPENDS std_msgs sensor_msgs geometry_msgs message_runtime
    # CATKIN_DEPENDS roscpp rospy std_msgs message_runtime
#  DEPENDS system_lib
)

include_directories(
# include
# ${catkin_INCLUDE_DIRS}
)

