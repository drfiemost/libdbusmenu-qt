set(qtapp_SRCS
    main.cpp
    )

add_executable(dbusmenubench-qtapp ${qtapp_SRCS})

include_directories(
    ${CMAKE_CURRENT_SOURCE_DIR}/../../src
    ${CMAKE_CURRENT_BINARY_DIR}/../../src
    ${QJSON_INCLUDE_DIR}
    )

target_link_libraries(dbusmenubench-qtapp
    dbusmenu-qt
    Qt4::QtGui
    Qt4::QtCore
    Qt4::QtDBus
    ${QJSON_LIBRARIES}
    )
