package(go_import_path = "github.com/thought-machine/please")

go_library(
    name = "hooks",
    srcs = ["hooks.go"],
    hooks = [
        ":testing",
    ],
)

go_hook(
    name = "testing",
    cmd = 'echo "colton was here" > $OUT',
    outs = ["colton_was_here.txt"],
    tools=[CONFIG.GO_TOOL],
)

go_test(
    name = "hooks_test",
    srcs = ["hooks.go"],
    external = True,
    deps = [
        ":hooks",
        "//third_party/go:testify",
    ],
)
