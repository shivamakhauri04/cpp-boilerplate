set(GTEST_SHUFFLE 1)

add_executable(
    cpp-test
    main.cpp
    basePID.h
    ParentPIDGmockStatic.h
    PID_Controller_test.cpp
    ../app/PID_Controller.cpp
    ../app/PID_Interface.cpp
)

target_include_directories(cpp-test PUBLIC ../vendor/googletest/googletest/include PUBLIC ../vendor/googletest/googlemock/include ${CMAKE_SOURCE_DIR}/include)

target_link_libraries(cpp-test PUBLIC gtest PUBLIC gmock)
