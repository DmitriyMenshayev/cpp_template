set(TargetName main)

add_executable(${TargetName}
    main.cpp
)

target_include_directories(${TargetName} 
    PUBLIC 
        ${PROJECT_SOURCE_DIR}/include
)

target_link_directories(${TargetName}
    PUBLIC 
        ${PROJECT_SOURCE_DIR}/lib
)
 
target_link_libraries(${TargetName} ) 