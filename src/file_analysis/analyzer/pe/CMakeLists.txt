include(BroPlugin)

include_directories(BEFORE ${CMAKE_CURRENT_SOURCE_DIR}
                           ${CMAKE_CURRENT_BINARY_DIR})

bro_plugin_begin(Bro PE)
bro_plugin_cc(PE.cc Plugin.cc)
bro_plugin_bif(events.bif)
bro_plugin_pac(
  pe.pac
  pe-analyzer.pac
  pe-file-headers.pac
  pe-file-idata.pac
  pe-file.pac
  pe-file-types.pac
)
bro_plugin_end()
