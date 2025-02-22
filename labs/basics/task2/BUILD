load("@rules_qt//:qt.bzl", "qt_cc_binary", "qt_cc_library", "qt_ui_library", "qt_resource")

qt_resource(
    name = "resources",
    files = ["resources.qrc"],
)

qt_ui_library(
    name = "ui_main_window",
    srcs = ["mainwindow.ui"],
)

qt_cc_library(
    name = "main_window",
    srcs = ["mainwindow.cpp"],
    hdrs = ["mainwindow.h", "ui_mainwindow.h"],
    deps = [
        ":ui_main_window",
        ":resources",
        "@rules_qt//:qt_core",
        "@rules_qt//:qt_gui",
        "@rules_qt//:qt_widgets",
    ],
)

qt_cc_binary(
    name = "task2",
    srcs = ["main.cpp"],
    deps = [
        ":main_window",
        "@rules_qt//:qt_widgets",
    ],
)
