cmake_minimum_required(VERSION 2.8)
project( simple-vo )
find_package( OpenCV 3.0 REQUIRED )

set(CMAKE_INCLUE_CURRENT_DIR ON)
#set(CMAKE_BUILD_TYPE RELEASE)
#set(CMAKE_CONFIGURATION_TYPES RELEASE)

include_directories( ${OpenCV_INCLUDE_DIRS} )

add_executable(simple_vo "src/Frame.hpp" "src/Frame.cpp" "src/MathOperations.h" "src/camera.hpp" "src/camera.cpp" "src/main.cpp")
target_link_libraries(simple_vo ${OpenCV_LIBS})