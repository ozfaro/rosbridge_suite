cmake_minimum_required(VERSION 2.8.3)
project(rosbridge_server)

find_package(catkin REQUIRED)

catkin_python_setup()

catkin_package()

install(PROGRAMS
  scripts/rosbridge_websocket.py
  scripts/rosbridge_tcp.py
  scripts/rosbridge_udp.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

install(FILES
  launch/rosbridge_websocket.launch
  launch/rosbridge_tcp.launch
  launch/rosbridge_udp.launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch
)

