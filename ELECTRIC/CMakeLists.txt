# Compile MDI
add_subdirectory(mdi)
add_subdirectory(pytest)

# Add an __init__.py to the MDI directory, so that it can be used as a package
file(WRITE ${CMAKE_CURRENT_BINARY_DIR}/mdi/__init__.py "")

# Compile the driver
configure_file(${CMAKE_CURRENT_SOURCE_DIR}/ELECTRIC.py ${CMAKE_CURRENT_BINARY_DIR}/ELECTRIC.py COPYONLY)
configure_file(${CMAKE_CURRENT_SOURCE_DIR}/util.py ${CMAKE_CURRENT_BINARY_DIR}/util.py COPYONLY)
