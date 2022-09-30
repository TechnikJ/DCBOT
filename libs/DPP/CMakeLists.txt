message("-- Linkin DPP")
add_library(dpp SHARED IMPORTED)
set_property(TARGET dpp PROPERTY
             IMPORTED_LOCATION "lib/bin/dpp.dll")
set_property(TARGET dpp PROPERTY
             IMPORTED_IMPLIB "lib/dpp-10.0/dpp.lib")

set_target_properties(dpp PROPERTIES LINKER_LANGUAGE CXX)