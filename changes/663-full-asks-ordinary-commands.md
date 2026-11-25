---
section: fixed
---

- **Full no longer asks for ordinary commands in a worktree.** Commands that name where the shell is (`cd "$(pwd)/apps/web"`, `Set-Location (Get-Location)`) run without asking again at Full and Auto, and no level asks any more for a name of three or more dots in the worktree (`go test ./...`, a `'...'` in a one-liner), which counted as CodeDen's own home because session worktrees live there.
