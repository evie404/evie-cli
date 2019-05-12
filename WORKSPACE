load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "io_bazel_rules_go",
    urls = ["https://github.com/bazelbuild/rules_go/releases/download/0.18.4/rules_go-0.18.4.tar.gz"],
    sha256 = "3743a20704efc319070957c45e24ae4626a05ba4b1d6a8961e87520296f1b676",
)

http_archive(
    name = "bazel_gazelle",
    urls = ["https://github.com/bazelbuild/bazel-gazelle/releases/download/0.17.0/bazel-gazelle-0.17.0.tar.gz"],
    sha256 = "3c681998538231a2d24d0c07ed5a7658cb72bfb5fd4bf9911157c0e9ac6a2687",
)

http_archive(
    name = "com_github_bazelbuild_buildtools",
    strip_prefix = "buildtools-882724efbd6169961bac0932892bcc0281c6d6f5",
    url = "https://github.com/bazelbuild/buildtools/archive/882724efbd6169961bac0932892bcc0281c6d6f5.zip",
)

load("@io_bazel_rules_go//go:deps.bzl", "go_rules_dependencies", "go_register_toolchains")

go_rules_dependencies()

go_register_toolchains()

load("@bazel_gazelle//:deps.bzl", "gazelle_dependencies", "go_repository")

gazelle_dependencies()

load("@com_github_bazelbuild_buildtools//buildifier:deps.bzl", "buildifier_dependencies")

buildifier_dependencies()

go_repository(
    name = "org_golang_x_oauth2",
    commit = "9f3314589c9a9136388751d9adae6b0ed400978a",
    importpath = "golang.org/x/oauth2",
)

go_repository(
    name = "com_github_google_go_github",
    commit = "2680886eeed75abb99132edfa256066dd05d65c9",
    importpath = "github.com/google/go-github",
)

go_repository(
    name = "com_github_google_go_querystring",
    commit = "c8c88dbee036db4e4808d1f2ec8c2e15e11c3f80",
    importpath = "github.com/google/go-querystring",
)
