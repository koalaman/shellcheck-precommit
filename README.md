# ShellCheck pre-commit hook

This is the official [pre-commit hook](https://pre-commit.com/) for
[ShellCheck](https://github.com/koalaman/shellcheck),
the static analysis tool for shell scripts.

Activate by adding it to your `.pre-commit-config.yaml`:

```sh
repos:
-   repo: https://github.com/koalaman/shellcheck-precommit
    rev: v0.4.6
    hooks:
    -   id: shellcheck
#       args: ["--severity=warning"]  # Optionally only show errors and warnings
```

#### Why a separate repo?

This repo keeps the pre-commit hook out of the critical path of ShellCheck
releases, reducing the number of things that can go wrong. This in turn helps
ensure a smoother `pre-commit autoupdate`. 

