cmake_minimum_required(VERSION 3.2)
project(ComponentePC)

set(sources main.cpp ComponentaPC.cpp ComponentaPC.h Header.h)
add_executable(${PROJECT_NAME} ${sources})
set(CMAKE_CONFIGURATION_TYPES Release)
set_target_properties(${PROJECT_NAME} PROPERTIES  CXX_STANDARD 14)
set(CMAKE_CXX_FLAGS_RELEASE "${CMAKE_CXX_FLAGS_RELEASE} /Ot")

install(TARGETS ${PROJECT_NAME} DESTINATION bin)
install(FILES ${sources} DESTINATION src)
