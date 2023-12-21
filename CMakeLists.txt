cmake_minimum_required(VERSION 3.8)
# プロジェクト名を指定する
project(test_joystick VERSION 0.1.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
#set(CMAKE_CXX_COMPILER "/usr/bin/g++-10") # Update the compiler version
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++17") # Set the C++ standard
set(CMAKE_EXE_LINKER_FLAGS "-fuse-ld=gold") # Update the linker version

find_package(Threads)

# インクルードパスを追加

add_executable(${CMAKE_PROJECT_NAME} 
    main.cpp
)

if(WIN32)
	target_link_libraries(${CMAKE_PROJECT_NAME} ws2_32)
else()
    target_link_libraries(${CMAKE_PROJECT_NAME} ${CMAKE_THREAD_LIBS_INIT})
endif()
