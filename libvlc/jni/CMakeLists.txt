
cmake_minimum_required(VERSION 3.4.1)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=gnu++11")

add_library(libvlcjni SHARED IMPORTED)

set_property(TARGET libvlcjni
             PROPERTY IMPORTED_LOCATION
             ${CMAKE_CURRENT_SOURCE_DIR}/../native-libs/${ANDROID_ABI}/libvlcjni.so)

# target_link_libraries(libvlcjni
#                       ${CMAKE_CURRENT_SOURCE_DIR}/../native-libs/${ANDROID_ABI}/libanw.21.so
#                       ${CMAKE_CURRENT_SOURCE_DIR}/../native-libs/${ANDROID_ABI}/libvlc.so)
