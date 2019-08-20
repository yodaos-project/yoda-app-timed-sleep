cmake_minimum_required(VERSION 3.0)
project(yodaos-timed-sleep CXX)
set(CMAKE_CXX_STANDARD 11)

# MARK: - timed-sleep
set(APP_ROOT_DIR "/opt/apps/timed-sleep")
set(APP_INSTALL_DIR "${CMAKE_INSTALL_DIR}${APP_ROOT_DIR}")

file(GLOB TIMED_SLEEP_SRC *.js *.json)

install(FILES ${TIMED_SLEEP_SRC}
  DESTINATION ${APP_INSTALL_DIR}
  PERMISSIONS OWNER_READ OWNER_WRITE GROUP_READ WORLD_READ)
