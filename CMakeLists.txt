cmake_minimum_required(VERSION 3.17)

set(CMAKE_CXX_STANDARD 17)
set(PROJECT_NAME AsioApp)

project(${PROJECT_NAME})
 
# find set and boost
set(BOOST_ROOT "external/boost_1_79_0")
set(Boost_USE_STATIC_LIBS ON)

find_package(Boost)
 
# include boost
include_directories(${Boost_INCLUDE_DIR})
add_executable(${PROJECT_NAME} Src/main.cpp)
target_link_libraries(${PROJECT_NAME} ${Boost_LIBRARIES})
