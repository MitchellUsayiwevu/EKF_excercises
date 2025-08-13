cmake_minimum_required(VERSION 3.7)
project(EKF_EXERCISES)

# Use C++17
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Extra compiler warnings
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall")

# If Eigen3 is installed system-wide
find_package(Eigen3 REQUIRED)

add_executable(EKF_2D
        main.cpp
        kalman_filter.cpp
        tracking.cpp
)

target_link_libraries(EKF_2D Eigen3::Eigen)