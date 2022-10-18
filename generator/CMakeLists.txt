set(generator_sources
    graph_generator.c
    make_graph.c
    splittable_mrg.c
    utils.c
)

add_library(generator ${generator_sources})
target_link_libraries(generator PUBLIC OpenMP::OpenMP_C)
target_include_directories(generator PUBLIC ${CMAKE_CURRENT_LIST_DIR})
target_compile_definitions(generator PRIVATE GRAPH_GENERATOR_OMP)
