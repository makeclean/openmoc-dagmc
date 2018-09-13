project(dagmc-openmoc)
cmake_minimum_required(VERSION 2.8)
message(STATUS "Buidling DAGMC-OPENMOC")

# Allow use of find_package(HDF5), find_package(MOAB), etc.
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_CURRENT_LIST_DIR}/cmake)

# Make sure we have MOAB
find_package(MOAB REQUIRED)

# Make sure we have DAGMC
find_package(DAGMC REQUIRED)

# openmoc needs openmp
find_package(OpenMP REQUIRED)

# do stuff
add_subdirectory(src)
