cmake_minimum_required(VERSION 3.16)

project(VulkanEngine LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
find_package(Vulkan REQUIRED)
file(GLOB SOURCES "src/*.cpp")


add_executable(VulkanEngine ${SOURCES})
target_link_libraries(VulkanEngine glfw3 Vulkan::Vulkan)

