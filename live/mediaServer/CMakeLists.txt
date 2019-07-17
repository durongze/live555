cmake_minimum_required(VERSION 3.4.1)
# close openssl
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -DDYZ_DBG")

file(GLOB MEDIA_SERVER_SRC *.cpp *.hh include/*.hh)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../BasicUsageEnvironment/include 
				${CMAKE_CURRENT_SOURCE_DIR}/../groupsock/include 
				${CMAKE_CURRENT_SOURCE_DIR}/../UsageEnvironment/include 
				${CMAKE_CURRENT_SOURCE_DIR}/../liveMedia/include )
add_executable(mediaServer ${MEDIA_SERVER_SRC} )
target_link_libraries(mediaServer ws2_32.lib BasicUsageEnvironment.lib GroupSock.lib liveMedia.lib UsageEnvironment.lib)
