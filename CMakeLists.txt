# Generated from qtsvg.pro.

cmake_minimum_required(VERSION 3.15.0)

include(.cmake.conf)
project(QtSvg
    VERSION "${QT_REPO_MODULE_VERSION}"
    DESCRIPTION "Qt SVG Libraries" # special case
    HOMEPAGE_URL "https://qt.io/"
    LANGUAGES CXX C
)

# special case begin
# Make sure we only use latest private CMake API, aka no compatibility wrappers.
set(QT_NO_INTERNAL_COMPATIBILITY_FUNCTIONS TRUE)
# special case end

find_package(Qt6 ${PROJECT_VERSION} CONFIG REQUIRED COMPONENTS BuildInternals Core Gui Widgets) # special case
find_package(Qt6 ${PROJECT_VERSION} CONFIG OPTIONAL_COMPONENTS Xml) # special case for tests
qt_build_repo()
