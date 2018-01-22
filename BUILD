load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "c.go",
        "const.go",
        "const_auto.go",
        "group.go",
        "group_intern.c",
        "group_intern.go",
        "group_legacy.go",
        "hooks.go",
        "options.go",
        "tox.go",
        "toxav.go",
        "toxencryptsave.go",
        "userdata.go",
        "userdata_legacy.go",
        "utils.go",
        "yuv2rgb.c",
    ],
    cdeps = ["//c-toxcore"],
    cgo = True,
    copts = ["-g -O2 -std=c99 -Wall"],
    importpath = "github.com/TokTok/go-toxcore-c",
    visibility = ["//visibility:public"],
    deps = [
        "@com_github_sasha_s_go_deadlock//:go_default_library",
        "@com_github_streamrail_concurrent_map//:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "group_test.go",
        "tox_test.go",
    ],
    embed = [":go_default_library"],
    importpath = "github.com/TokTok/go-toxcore-c",
)
