cmake_minimum_required(VERSION 3.8)
project(exercise_pkg)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# find dependencies
find_package(ament_cmake REQUIRED)
# uncomment the following section in order to fill in
# further dependencies manually.
# find_package(<dependency> REQUIRED)

if(BUILD_TESTING)
  find_package(ament_lint_auto REQUIRED)
  ament_lint_auto_find_test_dependencies()
  # Optional: Skip certain linters if not needed
  # set(ament_cmake_cpplint_FOUND TRUE)
  # set(ament_cmake_copyright_FOUND TRUE)
endif()

# Install launch files
install(DIRECTORY launch
  DESTINATION share/${PROJECT_NAME})

ament_package()
