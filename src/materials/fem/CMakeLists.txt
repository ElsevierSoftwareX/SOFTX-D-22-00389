# add_subdirectory (unit_test)
#
# Add subdirectories
#
# add_subdirectory (unit_test)
# Collection of libs that we need to link with
set(FEM_SOURCES
    FEM_routines.cxx
)

# PdFEMUtilities library
add_library(FEMUtilities ${FEM_SOURCES})

IF(INSTALL_PERIDIGM)
    install(TARGETS FEMUtilities EXPORT peridigm-export
        LIBRARY DESTINATION ${LIB_INSTALL_DIR}
        ARCHIVE DESTINATION ${LIB_INSTALL_DIR})
ENDIF()
