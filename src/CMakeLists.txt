set(TargetName main)

add_executable(${TargetName}
    main.cpp
)

target_include_directories(${TargetName} 
    PUBLIC 
        ${PROJECT_SOURCE_DIR}/include
)

target_include_directories(${TargetName} 
    PUBLIC 
        ${CMAKE_SOURCE_DIR}/third_party/OpenCL-SDK/external/OpenCL-Headers
)

target_link_directories(${TargetName}
    PUBLIC 
        ${PROJECT_SOURCE_DIR}/lib
)
 
target_link_libraries(${TargetName} OpenCL)

target_compile_definitions(${TargetName} PRIVATE CL_TARGET_OPENCL_VERSION=120)