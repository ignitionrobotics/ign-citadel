cmake_minimum_required(VERSION 3.10.2 FATAL_ERROR)

#============================================================================
# Initialize the project
#============================================================================
project(ignition-citadel VERSION 1.0.1)

#============================================================================
# Find ignition-cmake
#============================================================================
# If you get an error at this line, you need to install ignition-cmake
find_package(ignition-cmake2 2.0.0 REQUIRED)

#============================================================================
# Configure the project
#============================================================================
ign_configure_project()

# all list of citadel packages

ign_find_package(ignition-common3 REQUIRED VERSION 3.4)
ign_find_package(ignition-fuel_tools4 REQUIRED VERSION 4.1)
ign_find_package(ignition-gazebo3 REQUIRED VERSION 3.3)
ign_find_package(ignition-gui3 REQUIRED VERSION 3.1)
ign_find_package(ignition-launch2 REQUIRED)
ign_find_package(ignition-math6 REQUIRED VERSION 6.6)
ign_find_package(ignition-msgs5 REQUIRED VERSION 5.3)
ign_find_package(ignition-physics2 REQUIRED VERSION 2.3)
ign_find_package(ignition-plugin1 REQUIRED)
ign_find_package(ignition-rendering3 REQUIRED VERSION 3.1)
ign_find_package(ignition-sensors3 REQUIRED)
ign_find_package(ignition-tools REQUIRED)
ign_find_package(ignition-transport8 REQUIRED)
ign_find_package(sdformat9 REQUIRED VERSION 9.2.0)

install(DIRECTORY gazebodistro DESTINATION ${IGN_DATA_INSTALL_DIR})
