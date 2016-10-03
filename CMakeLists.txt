#
# project: fips-nlohmann-json
#

if (NOT FIPS_IMPORT)
    cmake_minimum_required(VERSION 2.8)
    get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
    include("${FIPS_ROOT_DIR}/cmake/fips.cmake")
    fips_setup()
    fips_project(fips-nlohmann-json)
endif()

fips_begin_lib(nlohmann-json)
    fips_dir(json/src GROUP .)
    fips_files(json.hpp)
fips_end_lib()

if (NOT FIPS_IMPORT)
    fips_finish()
endif()


