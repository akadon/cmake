cmake_minimum_required (VERSION 3.20)
project(build)

# settings

    set(CMAKE_BUILD_TYPE "Debug")  
    #set(CMAKE_BUILD_TYPE "Release")  
    #set(CMAKE_BUILD_TYPE "Dist")  

    set (CMAKE_EXPORT_COMPILE_COMMANDS ON)  
    set (CMAKE_LIBRARY_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/bin)
    set (CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/bin)

    set(CMAKE_CXX_STANDARD_REQUIRED ON)
    set(CMAKE_CXX_STANDARD 20)
    
# includes
    # add_subdirectory(vendor)

    # file(GLOB_RECURSE lib_inc_a src/**.h)
    # add_library(build SHARED empty.cpp ${lib_inc_a})
    # target_include_directories(build PUBLIC /src)

    # target_link_libraries(build PUBLIC 
    #     C:/VulkanSDK/1.2.182.0/Lib/vulkan-1.lib
    #     test
    # )

    #target_precompile_headers(build PUBLIC src/hzpch.h)

# executable
project(main)
    add_executable(main main.cpp)
    #target_include_directories(main PUBLIC build)
    #target_link_libraries(main PUBLIC build)
