---
section: security
---

- **Paths built from where the shell is resolve to that folder.** Writing beside the worktree that way (`rm -rf "$(pwd)/../x"`, `"$PWD../x"`) now asks, and so does a `cd` to the folder `pwd`, `Get-Location` or `git rev-parse --show-toplevel` prints once the command line redefines them or changes `PATH`.
- **Windows device paths and empty PowerShell values in a path now ask.** `\\?\C:\…`, `\\.\C:\…` and `\??\C:\…` name the same file as `C:\…`, so CodeDen's own home and credentials ask at every level in those forms too. A path that starts with or holds `$null`, `$true`, `$false` or `$_`, which a shell may expand to nothing, asks at Auto and Full. Alone (`> $null`, `Remove-Item $_`), they still run freely.
