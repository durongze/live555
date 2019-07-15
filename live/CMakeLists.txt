cmake_minimum_required(VERSION 3.4.1)
add_subdirectory(BasicUsageEnvironment)
add_subdirectory(groupsock)
add_subdirectory(liveMedia)
add_subdirectory(mediaServer)
add_subdirectory(proxyServer)
add_subdirectory(testProgs)
add_subdirectory(UsageEnvironment)
add_subdirectory(WindowsAudioInputDevice)

project(Live555)

add_compile_options(-DDYZ_DBG)

