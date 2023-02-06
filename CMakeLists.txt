cmake_minimum_required(VERSION 3.5)
project(aravis_vendor)

find_package(ament_cmake REQUIRED)

list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake/modules")

#  Default aravis-0.8, TODO(pan): add support for aravis-0.6
find_package(Aravis REQUIRED)
find_package(GLIB REQUIRED)
find_package(GStreamer REQUIRED)

install(DIRECTORY cmake DESTINATION share/${PROJECT_NAME})

ament_cmake(
  CONFIG_EXTRAS "aravis_vendor-extras.cmake"
)