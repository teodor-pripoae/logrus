load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "logrus",
    srcs = [
        "alt_exit.go",
        "buffer_pool.go",
        "doc.go",
        "entry.go",
        "exported.go",
        "formatter.go",
        "hooks.go",
        "json_formatter.go",
        "logger.go",
        "logrus.go",
        "terminal_check_bsd.go",
        "terminal_check_js.go",
        "terminal_check_no_terminal.go",
        "terminal_check_notappengine.go",
        "terminal_check_solaris.go",
        "terminal_check_unix.go",
        "terminal_check_windows.go",
        "text_formatter.go",
        "writer.go",
    ],
    importpath = "github.com/sirupsen/logrus",
    visibility = ["//visibility:public"],
    deps = select({
        "@io_bazel_rules_go//go/platform:aix": [
            "@org_golang_x_sys//unix",
        ],
        "@io_bazel_rules_go//go/platform:android": [
            "@org_golang_x_sys//unix",
        ],
        "@io_bazel_rules_go//go/platform:darwin": [
            "@org_golang_x_sys//unix",
        ],
        "@io_bazel_rules_go//go/platform:dragonfly": [
            "@org_golang_x_sys//unix",
        ],
        "@io_bazel_rules_go//go/platform:freebsd": [
            "@org_golang_x_sys//unix",
        ],
        "@io_bazel_rules_go//go/platform:illumos": [
            "@org_golang_x_sys//unix",
        ],
        "@io_bazel_rules_go//go/platform:ios": [
            "@org_golang_x_sys//unix",
        ],
        "@io_bazel_rules_go//go/platform:linux": [
            "@org_golang_x_sys//unix",
        ],
        "@io_bazel_rules_go//go/platform:netbsd": [
            "@org_golang_x_sys//unix",
        ],
        "@io_bazel_rules_go//go/platform:openbsd": [
            "@org_golang_x_sys//unix",
        ],
        "@io_bazel_rules_go//go/platform:solaris": [
            "@org_golang_x_sys//unix",
        ],
        "@io_bazel_rules_go//go/platform:windows": [
            "@org_golang_x_sys//windows",
        ],
        "//conditions:default": [],
    }),
)

alias(
    name = "go_default_library",
    actual = ":logrus",
    visibility = ["//visibility:public"],
)

go_test(
    name = "logrus_test",
    srcs = [
        "alt_exit_test.go",
        "entry_test.go",
        "example_basic_test.go",
        "example_custom_caller_test.go",
        "example_default_field_value_test.go",
        "example_function_test.go",
        "example_global_hook_test.go",
        "example_hook_test.go",
        "formatter_bench_test.go",
        "hook_test.go",
        "json_formatter_test.go",
        "level_test.go",
        "logger_bench_test.go",
        "logger_test.go",
        "logrus_test.go",
        "text_formatter_test.go",
        "writer_test.go",
    ],
    embed = [":logrus"],
    deps = [
        "//hooks/test",
        "//internal/testutils",
        "@com_github_stretchr_testify//assert",
        "@com_github_stretchr_testify//require",
    ] + select({
        "@io_bazel_rules_go//go/platform:aix": [
            "//hooks/syslog",
        ],
        "@io_bazel_rules_go//go/platform:android": [
            "//hooks/syslog",
        ],
        "@io_bazel_rules_go//go/platform:darwin": [
            "//hooks/syslog",
        ],
        "@io_bazel_rules_go//go/platform:dragonfly": [
            "//hooks/syslog",
        ],
        "@io_bazel_rules_go//go/platform:freebsd": [
            "//hooks/syslog",
        ],
        "@io_bazel_rules_go//go/platform:illumos": [
            "//hooks/syslog",
        ],
        "@io_bazel_rules_go//go/platform:ios": [
            "//hooks/syslog",
        ],
        "@io_bazel_rules_go//go/platform:js": [
            "//hooks/syslog",
        ],
        "@io_bazel_rules_go//go/platform:linux": [
            "//hooks/syslog",
        ],
        "@io_bazel_rules_go//go/platform:netbsd": [
            "//hooks/syslog",
        ],
        "@io_bazel_rules_go//go/platform:openbsd": [
            "//hooks/syslog",
        ],
        "@io_bazel_rules_go//go/platform:plan9": [
            "//hooks/syslog",
        ],
        "@io_bazel_rules_go//go/platform:solaris": [
            "//hooks/syslog",
        ],
        "//conditions:default": [],
    }),
)
