cmake_minimum_required(VERSION 3.5)

project(heera-kwin-plugins)

set(PROJECT_NAME "heera-kwin")

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTORCC ON)

add_subdirectory(plugins)

install(FILES config/kwinrc DESTINATION /etc/xdg)
install(DIRECTORY scripts/heeralauncher DESTINATION /usr/share/kwin/scripts)
install(DIRECTORY scripts/heera_squash DESTINATION /usr/share/kwin/effects)
install(DIRECTORY tabbox/heera_thumbnail DESTINATION /usr/share/kwin/tabbox)
