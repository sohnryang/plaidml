package(default_visibility = ["//visibility:public"])

filegroup(
    name = "empty",
    srcs = [],
)

exports_files([
    "setup.tpl.py",
    "venv.tpl.py",
    "version.tpl.cc",
])

cc_toolchain_suite(
    name = "toolchain",
    toolchains = {
        "arm7-linux|gcc": ":cc-gcc-arm7linux",
    },
)

config_setting(
    name = "x64-linux",
    values = {"cpu": "k8"},
    visibility = ["//visibility:public"],
)

# The cpu flags are left on to ensure these matches are more precise
config_setting(
    name = "x64-ubuntu-14.04",
    define_values = {"VARIANT": "ubuntu-14.04"},
    values = {"cpu": "k8"},
    visibility = ["//visibility:public"],
)

config_setting(
    name = "x64-ubuntu-17.04",
    define_values = {"VARIANT": "ubuntu-17.04"},
    values = {"cpu": "k8"},
    visibility = ["//visibility:public"],
)

config_setting(
    name = "arm7-ubuntu-14.04",
    define_values = {"VARIANT": "arm7-ubuntu-14.04"},
    values = {"cpu": "arm7-linux"},
    visibility = ["//visibility:public"],
)

config_setting(
    name = "darwin",
    values = {"cpu": "darwin"},
    visibility = ["//visibility:public"],
)

config_setting(
    name = "android",
    values = {
        "android_crosstool_top": "@androidndk//:toolchain-libcpp",
    },
)

config_setting(
    # Native compilation on Windows.
    name = "x64_windows",
    values = {"cpu": "x64_windows"},
    visibility = ["//visibility:public"],
)

config_setting(
    name = "with_callgrind",
    define_values = {"with_callgrind": "true"},
    visibility = ["//visibility:public"],
)

cc_toolchain(
    name = "cc-gcc-arm7linux",
    all_files = ":empty",
    compiler_files = ":empty",
    cpu = "arm7-linux",
    dwp_files = ":empty",
    dynamic_runtime_libs = [":empty"],
    linker_files = ":empty",
    objcopy_files = ":empty",
    static_runtime_libs = [":empty"],
    strip_files = ":empty",
    supports_param_files = 1,
    visibility = ["//visibility:public"],
)
