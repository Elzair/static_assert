cmake_minimum_required(VERSION 3.3)

project(boost_static_assert)

add_library(boost_static_assert INTERFACE)

target_include_directories(boost_static_assert BEFORE INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)

install(TARGETS boost_static_assert DESTINATION lib)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/boost DESTINATION include)

add_library(boost::static_assert ALIAS boost_static_assert)
