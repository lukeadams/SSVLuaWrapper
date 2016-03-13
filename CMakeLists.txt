cmake_minimum_required(VERSION 3.0)
set(CPM_MODULE_NAME SSVLuaWrapper)
include(./cmake/modules/CPM-mod.cmake)

SET(SSVDepsRoot "https://github.com/lukeadams/")
CPM_AddModule("SSVCMake"
	GIT_REPOSITORY "${SSVDepsRoot}SSVCMake"
	GIT_TAG "cpm")
SET(CMAKE_MODULE_PATH ${CPM_KV_SOURCEDIR_MAP_SSVCMake}/cmake/modules ${CMAKE_MODULE_PATH})
include(SSVCMake)

CPM_ExportAdditionalIncludeDir("./include")
CPM_InitModule(${CPM_MODULE_NAME})
