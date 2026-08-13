cmake_minimum_required(VERSION 3.20)

project(nvibrant VERSION 1.0.0 LANGUAGES CXX)

add_executable(nvibrant
    nvibrant/main.cpp
)

target_include_directories(nvibrant PRIVATE
    open-gpu/src/nvidia-modeset/interface
    open-gpu/src/nvidia-modeset/include
    open-gpu/src/common/inc
    open-gpu/src/common/sdk/nvidia/inc
    open-gpu/src/common/unix/common/inc
)

install(TARGETS nvibrant
    RUNTIME DESTINATION bin
)