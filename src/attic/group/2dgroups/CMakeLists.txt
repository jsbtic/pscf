add_executable(new_2dgroups
    ${BUILD_MACOSX_BUNDLE} WIN32
	new_2dgroups.f
)
target_link_libraries(new_2dgroups LINK_PUBLIC common io scf rpa)

install(TARGETS new_2dgroups
        BUNDLE DESTINATION . COMPONENT Runtime
        RUNTIME DESTINATION bin COMPONENT Runtime
        LIBRARY DESTINATION lib COMPONENT Runtime
        ARCHIVE DESTINATION lib/static COMPONENT Runtime
)

set(APPS ${CMAKE_CURRENT_BINARY_DIR}/new_2dgroups${MACOSX_BUNDLE_EXT})
set(DIRS "")

if (BUILD_DMG)
# Copy libraries into the DMG
INSTALL(CODE "
   include(BundleUtilities)
   set (BU_CHMOD_BUNDLE_ITEMS ON)
   fixup_bundle(\"${APPS}\"   \"\"   \"${DIRS}\")
" COMPONENT Runtime)
endif (BUILD_DMG)
