# Contributing to TodoTik repositories

## Commit authorship policy

Developers are responsible for their commits. AI tools may assist with code,
but commits are authored by the human who reviews and approves them.

**Do not add AI co-authorship lines** (`Co-Authored-By:` referencing AI
assistants) to commit messages. A `commit-msg` hook in each repository
enforces this automatically.

## Git hooks setup

All repositories include a `.githooks/` directory with enforced hooks.
After cloning, configure git to use it:

```sh
git config core.hooksPath .githooks
```

To apply this automatically for all repos under a shared workspace directory,
add to your `~/.gitconfig`:

```gitconfig
[includeIf "gitdir:~/workspace/"]
    path = ~/workspace/.gitconfig-workspace
```

And create `~/workspace/.gitconfig-workspace`:

```gitconfig
[core]
    hooksPath = .githooks
```
