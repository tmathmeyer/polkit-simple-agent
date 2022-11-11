langs("C")

cc_binary(
  name = "polkit-dumb-agent-responder",
  srcs = [ "sendreply.c" ],
  compiler = "gcc",
  include_dirs = [
    "/usr/include/systemd",
  ],
  flags = [
    "-lsystemd"
  ],
)

cpp_header (
  name = "include",
  srcs = [
    "agent.h",
  ],
)

cc_binary(
  name = "polkit-dumb-agent",
  srcs = [
    "agent.cpp",
  ],
  includes = [
    ":include",
  ],
  include_dirs = [
    "/usr/include/qt/QtWidgets",
    "/usr/include/qt/QtGui",
    "/usr/include/qt/QtCore",
    "/usr/include/qt/QtDBus",
    "/usr/include/qt",
    "/usr/include/KF5/KDESu",
    "/usr/include/KF5",
    "/usr/include/KF5/KPty",
  ],
  flags = [
    "-lQtCore",
    "-lQtGui",
    "-DQT_CORE_LIB",
    "-DQT_DBUS_LIB",
    "-DQT_GUI_LIB",
    "-DQT_WIDGETS_LIB",
  ],
)