add_executable(com main.c)
target_link_libraries(com pico_stdlib hardware_uart com_lib function)
pico_add_extra_outputs(com)


