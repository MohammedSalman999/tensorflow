load("//tensorflow/compiler/mlir:glob_lit_test.bzl", "glob_lit_tests")
load("//tensorflow/tsl:tsl.default.bzl", "filegroup")

# copybara:uncomment package(default_applicable_licenses = ["//tensorflow:license"])

glob_lit_tests(
    data = [":test_utilities"],
    driver = "@llvm-project//mlir:run_lit.sh",
    test_file_exts = [
        "mlir",
    ],
)

# Bundle together all of the test utilities that are used by tests.
filegroup(
    name = "test_utilities",
    testonly = True,
    data = [
        "snapshot.mlir.pb",
        "//tensorflow/compiler/xla/mlir/tools/mlir_bisect:mlir-bisect",
        "@llvm-project//llvm:FileCheck",
        "@llvm-project//llvm:not",
    ],
)
