project(sizegripitemdemo)

INCLUDE_DIRECTORIES(${CMAKE_CURRENT_BINARY_DIR})
INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR}/..)

SET(sizegripitemdemo_SOURCES ../sizegripitem.cpp mainwindow.cpp main.cpp)
SET(sizegripitemdemo_HEADERS mainwindow.h)
SET(sizegripitemdemo_FORMS mainwindow.ui)

QT5_WRAP_CPP(sizegripitemdemo_HEADERS_MOC ${sizegripitemdemo_HEADERS})
QT5_WRAP_UI(sizegripitemdemo_FORMS_HEADERS ${sizegripitemdemo_FORMS})

ADD_EXECUTABLE(sizegripitemdemo
  ${sizegripitemdemo_SOURCES}
  ${sizegripitemdemo_HEADERS_MOC}
  ${sizegripitemdemo_FORMS_HEADERS})

TARGET_LINK_LIBRARIES(sizegripitemdemo Qt5::Core Qt5::Gui Qt5::Widgets)
