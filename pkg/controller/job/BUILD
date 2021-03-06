package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "jobcontroller.go",
        "utils.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/api/v1:go_default_library",
        "//pkg/apis/batch/v1:go_default_library",
        "//pkg/client/clientset_generated/clientset:go_default_library",
        "//pkg/client/clientset_generated/clientset/typed/core/v1:go_default_library",
        "//pkg/client/legacylisters:go_default_library",
        "//pkg/client/listers/batch/v1:go_default_library",
        "//pkg/client/record:go_default_library",
        "//pkg/controller:go_default_library",
        "//pkg/controller/informers:go_default_library",
        "//pkg/util/metrics:go_default_library",
        "//vendor:github.com/golang/glog",
        "//vendor:k8s.io/apimachinery/pkg/api/errors",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/v1",
        "//vendor:k8s.io/apimachinery/pkg/util/runtime",
        "//vendor:k8s.io/apimachinery/pkg/util/wait",
        "//vendor:k8s.io/client-go/tools/cache",
        "//vendor:k8s.io/client-go/util/workqueue",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "jobcontroller_test.go",
        "utils_test.go",
    ],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/v1:go_default_library",
        "//pkg/apis/batch/v1:go_default_library",
        "//pkg/client/clientset_generated/clientset:go_default_library",
        "//pkg/client/clientset_generated/clientset/fake:go_default_library",
        "//pkg/controller:go_default_library",
        "//pkg/controller/informers:go_default_library",
        "//vendor:k8s.io/apimachinery/pkg/api/equality",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/v1",
        "//vendor:k8s.io/apimachinery/pkg/util/rand",
        "//vendor:k8s.io/apimachinery/pkg/util/wait",
        "//vendor:k8s.io/apimachinery/pkg/watch",
        "//vendor:k8s.io/client-go/rest",
        "//vendor:k8s.io/client-go/testing",
        "//vendor:k8s.io/client-go/tools/cache",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)
