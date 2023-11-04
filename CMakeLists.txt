cmake_minimum_required(VERSION 3.26)
project(NetworkDemo)

set(CMAKE_CXX_STANDARD 17)

find_package(Boost REQUIRED COMPONENTS system)
find_package(CURL REQUIRED)

include_directories(${Boost_INCLUDE_DIRS})
include_directories(${CURL_INCLUDE_DIRS})

add_executable(NetworkDemo main.cpp)


target_link_libraries(NetworkDemo
        ${Boost_LIBRARIES}
        ${CURL_LIBRARIES}
        ws2_32
)
