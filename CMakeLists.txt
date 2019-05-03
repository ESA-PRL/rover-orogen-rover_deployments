PROJECT(rover_deployments)
cmake_minimum_required(VERSION 2.6)

SET (CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/.orogen/config")
INCLUDE(rover_deploymentsBase)

# FIND_PACKAGE(KDL)
# FIND_PACKAGE(OCL)

install(CODE "execute_process(COMMAND sudo setcap CAP_NET_RAW=ep ${CMAKE_INSTALL_PREFIX}/bin/control)")
