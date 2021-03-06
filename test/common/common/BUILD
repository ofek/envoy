licenses(["notice"])  # Apache 2

load(
    "//bazel:envoy_build_system.bzl",
    "envoy_cc_binary",
    "envoy_cc_fuzz_test",
    "envoy_cc_test",
    "envoy_package",
)

envoy_package()

envoy_cc_fuzz_test(
    name = "base64_fuzz_test",
    srcs = ["base64_fuzz_test.cc"],
    corpus = "base64_corpus",
    deps = ["//source/common/common:base64_lib"],
)

envoy_cc_test(
    name = "base64_test",
    srcs = ["base64_test.cc"],
    deps = [
        "//source/common/buffer:buffer_lib",
        "//source/common/common:base64_lib",
    ],
)

envoy_cc_test(
    name = "cleanup_test",
    srcs = ["cleanup_test.cc"],
    deps = ["//source/common/common:cleanup_lib"],
)

envoy_cc_test(
    name = "fmt_test",
    srcs = ["fmt_test.cc"],
    deps = [
        "//source/common/common:fmt_lib",
        "//source/common/common:logger_lib",
    ],
)

envoy_cc_test(
    name = "hash_test",
    srcs = ["hash_test.cc"],
    deps = ["//source/common/common:hash_lib"],
)

envoy_cc_test(
    name = "hex_test",
    srcs = ["hex_test.cc"],
    deps = ["//source/common/common:hex_lib"],
)

envoy_cc_test(
    name = "optional_test",
    srcs = ["optional_test.cc"],
    deps = ["//include/envoy/common:optional"],
)

envoy_cc_test(
    name = "log_macros_test",
    srcs = ["log_macros_test.cc"],
    deps = [
        "//source/common/common:logger_lib",
        "//test/mocks/http:http_mocks",
        "//test/mocks/network:network_mocks",
        "//test/mocks/upstream:upstream_mocks",
    ],
)

envoy_cc_test(
    name = "utility_test",
    srcs = ["utility_test.cc"],
    external_deps = [
        "abseil_strings",
    ],
    deps = [
        "//source/common/common:utility_lib",
        "//test/test_common:utility_lib",
    ],
)

envoy_cc_test(
    name = "to_lower_table_test",
    srcs = ["to_lower_table_test.cc"],
    deps = ["//source/common/common:to_lower_table_lib"],
)

envoy_cc_test(
    name = "callback_impl_test",
    srcs = ["callback_impl_test.cc"],
    deps = ["//source/common/common:callback_impl_lib"],
)

envoy_cc_test(
    name = "shared_memory_hash_set_test",
    srcs = ["shared_memory_hash_set_test.cc"],
    deps = [
        "//source/common/common:hash_lib",
        "//source/common/common:shared_memory_hash_set_lib",
    ],
)

envoy_cc_binary(
    name = "utility_speed_test",
    srcs = ["utility_speed_test.cc"],
    external_deps = [
        "abseil_strings",
        "benchmark",
    ],
    deps = [
        "//source/common/common:assert_lib",
        "//source/common/common:utility_lib",
    ],
)
