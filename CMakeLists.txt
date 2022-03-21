cmake_minimum_required(VERSION 3.12...3.22)

project(test-github-actions-download)

# Find, configure, and include Qt. The recommended way to make sure that the
# desired version of Qt is found is to pass -DQt5_DIR to cmake, e.g.:
#
#   cmake .. -DQt5_DIR="C:\Qt\5.15.2\msvc2019_64\lib\cmake\Qt5"
#
message(STATUS "[Qt]")
set(CMAKE_AUTOMOC ON)
find_package(Qt5 COMPONENTS Core Gui Widgets REQUIRED)
get_filename_component(QT_ROOT ${Qt5_DIR}/../../.. ABSOLUTE)
message(STATUS "Found Qt: ${VGC_QT_ROOT}")
message(STATUS "Version: ${Qt5_VERSION}")
