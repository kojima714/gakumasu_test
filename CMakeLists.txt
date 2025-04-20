cmake_minimum_required(VERSION 3.2)

project(myApp)

find_package(wxWidgets COMPONENTS core base)
include(${wxWidgets_USE_FILE})

add_executable(myApp WIN32
  main.cpp
)

target_compile_features(myApp PUBLIC cxx_std_14)

target_link_libraries(myApp ${wxWidgets_LIBRARIES})
