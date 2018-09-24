licenses(["notice"])  # Apache 2.0

package(default_visibility = ["//visibility:public"])

load("//:skylark_library.bzl", "skylark_library")

exports_files([
    "LICENSE",
    "lib.bzl",
])

filegroup(
    name = "test_deps",
    testonly = True,
    srcs = [
        "BUILD",
        "//lib:test_deps",
    ] + glob(["*.bzl"]),
)

skylark_library(
    name = "lib",
    srcs = ["lib.bzl"],
    deprecation = (
        "lib.bzl will go away in the future, please directly depend on the" +
        " module(s) needed as it is more efficient."
    ),
    deps = [
        "//lib:collections",
        "//lib:dicts",
        "//lib:new_sets",
        "//lib:partial",
        "//lib:paths",
        "//lib:selects",
        "//lib:sets",
        "//lib:shell",
        "//lib:structs",
        "//lib:types",
        "//lib:unittest",
        "//lib:versions",
    ],
)

skylark_library(
    name = "skylark_library",
    srcs = ["skylark_library.bzl"],
)
