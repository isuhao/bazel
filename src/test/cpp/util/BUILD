# Description:
#   C++ utility tests for Bazel
package(default_visibility = ["//visibility:public"])

filegroup(
    name = "srcs",
    srcs = glob(["**"]),
    visibility = ["//src/test/cpp:__pkg__"],
)

cc_test(
    name = "md5_test",
    srcs = ["md5_test.cc"],
    deps = [
        "//src/main/cpp/util",
        "//src/main/cpp/util:md5",
        "//third_party:gtest",
    ],
)

cc_test(
    name = "file_test",
    srcs = ["file_test.cc"],
    deps = [
        "//src/main/cpp/util:file",
        "//third_party:gtest",
    ],
)

cc_test(
    name = "file_platform_test",
    srcs = ["file_posix_test.cc"],
    tags = ["manual"],
    deps = [
        "//src/main/cpp/util:file",
        "//src/main/cpp/util:file_platform",
        "//third_party:gtest",
    ],
)

cc_test(
    name = "numbers_test",
    srcs = ["numbers_test.cc"],
    deps = [
        "//src/main/cpp/util",
        "//third_party:gtest",
    ],
)

cc_test(
    name = "strings_test",
    srcs = ["strings_test.cc"],
    shard_count = 2,
    deps = [
        "//src/main/cpp/util:strings",
        "//third_party:gtest",
    ],
)

test_suite(name = "all_tests")
