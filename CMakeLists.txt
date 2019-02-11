cmake_minimum_required(VERSION 3.13)
project(leidenalg)

set(CMAKE_CXX_STANDARD 14)

set(CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake/")
find_package(IGRAPH)

include_directories(include)

add_library(leidenalg
        include/CPMVertexPartition.h
        include/GraphHelper.h
        include/LinearResolutionParameterVertexPartition.h
        include/ModularityVertexPartition.h
        include/MutableVertexPartition.h
        include/Optimiser.h
        include/pynterface.h
        include/python_optimiser_interface.h
        include/python_partition_interface.h
        include/RBConfigurationVertexPartition.h
        include/RBERVertexPartition.h
        include/ResolutionParameterVertexPartition.h
        include/SignificanceVertexPartition.h
        include/SurpriseVertexPartition.h
        src/CPMVertexPartition.cpp
        src/GraphHelper.cpp
        src/LinearResolutionParameterVertexPartition.cpp
        src/ModularityVertexPartition.cpp
        src/MutableVertexPartition.cpp
        src/Optimiser.cpp
        src/RBConfigurationVertexPartition.cpp
        src/RBERVertexPartition.cpp
        src/ResolutionParameterVertexPartition.cpp
        src/SignificanceVertexPartition.cpp
        src/SurpriseVertexPartition.cpp)

target_link_libraries(leidenalg igraph)