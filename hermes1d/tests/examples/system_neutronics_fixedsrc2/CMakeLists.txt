project(example-system_neutronics_fixedsrc2)

add_executable(${PROJECT_NAME} main.cpp)
include (../../CMake.common)

set(BIN ${PROJECT_BINARY_DIR}/${PROJECT_NAME})
add_test(example-system_neutronics_fixedsrc2 ${BIN})
set_tests_properties(example-system_neutronics_fixedsrc2 PROPERTIES WILL_FAIL TRUE)

target_link_libraries(${PROJECT_NAME} ${HERMES_BIN})
