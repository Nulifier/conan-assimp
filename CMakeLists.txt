project(cmake_wrapper)

include(conanbuildinfo.cmake)
conan_basic_setup()

# Provide zlib
set(ASSIMP_BUILD_ZLIB 0)
set(ZLIB_FOUND 1)
set(ZLIB_INCLUDE_DIR ${CONAN_INCLUDE_DIRS_ZLIB})
set(ZLIB_LIBRARIES ${CONAN_LIBS_ZLIB})

add_subdirectory("source_subfolder")
