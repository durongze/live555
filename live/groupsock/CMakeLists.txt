cmake_minimum_required(VERSION 3.4.1)
# close openssl
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -DDYZ_DBG")

file(GLOB GROUP_SOCK_SRC *.cpp *.c include/*.hh)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../BasicUsageEnvironment/include 
				${CMAKE_CURRENT_SOURCE_DIR}/../groupsock/include 
				${CMAKE_CURRENT_SOURCE_DIR}/../UsageEnvironment/include 
				${CMAKE_CURRENT_SOURCE_DIR}/../liveMedia/include 
				E:/program/zlib/include/ E:/program/openssl/include/ )
add_library(GroupSock.lib 
            STATIC
            ${GROUP_SOCK_SRC}
)
