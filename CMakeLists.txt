cmake_minimum_required(VERSION 2.8)
project(TP_MEDEV_6)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} $ENV{OSG_ROOT}/CMakeModules )

set(SRCEXT "cpp")

file(GLOB
source_files
*.${SRCEXT}
)

find_package(OpenSceneGraph 2.0 REQUIRED osg osgDB osgUtil osgViewer osgGA)
#find_package (OpenSceneGraph OSG OSGDB OSGUTIL OSGVIEWER)
INCLUDE_DIRECTORIES(${OSG_INCLUDE_DIR})

#augmentation
add_executable(tpavion ${source_files})

TARGET_LINK_LIBRARIES(tpavion ${OPENSCENEGRAPH_LIBRARIES})
message("OPENSCENEGRAPH_LIBRARY =  ${OPENSCENEGRAPH_LIBRARIES}")
