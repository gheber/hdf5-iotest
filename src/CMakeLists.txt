set(CMAKE_INCLUDE_CURRENT_DIR_IN_INTERFACE ON)

add_executable(hdf5_iotest
  configuration.c
  dataset.c
  hdf5_iotest.c
  ini.c
  read_test.c
  utils.c
  write_test.c)

include_directories(
  ${HDF5_INCLUDE_DIRS}
  ${MPI_INCLUDE_DIRS}
  ${UUID_INCLUDE_DIRS})

target_link_libraries(hdf5_iotest PUBLIC
  ${HDF5_LIBRARIES}
  ${MPI_LIBRARIES}
  ${UUID_LIBRARIES})
