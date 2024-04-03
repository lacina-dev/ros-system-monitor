cmake_minimum_required(VERSION 3.10.2)
project(system_monitor)

find_package(catkin)

catkin_package()

catkin_install_python(PROGRAMS
  bin/cpu_monitor.py
  bin/hdd_monitor.py
  bin/mem_monitor.py
  bin/net_monitor.py
  bin/ntp_monitor.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})

install(DIRECTORY
  config/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/config
)

install(DIRECTORY
  launch/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch
)
