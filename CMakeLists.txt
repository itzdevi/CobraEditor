cmake_minimum_required(VERSION 3.15.0)
project(CobraEditor VERSION 0.0.1)

file(GLOB SRCS
    src/*.c
    include/*.h
    src/**/*.c
    include/**/*.h
)

include_directories(Cobra/include)
add_subdirectory(Cobra)
add_executable(${PROJECT_NAME} ${SRCS})
target_link_libraries(${PROJECT_NAME} Cobra)