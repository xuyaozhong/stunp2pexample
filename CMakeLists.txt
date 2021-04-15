set(udpstunserver "udpstunserver")
set(udpstunclient "udpstunclient")


add_executable(${udpstunserver} udpstunserver.c)
add_executable(${udpstunclient} udpstunclient.c)


target_link_libraries(${udpstunserver} -lpthread -lmosquitto -ljson-c)
target_link_libraries(${udpstunclient} -lpthread -lmosquitto -ljson-c)

