# Contributing to TodoTik repositories

## Commit authorship policy

Developers are responsible for their commits. AI tools may assist with code,
but commits are authored by the people who review and approve them.

**Co-/authorship is strictly for natural persons, or omitted.** A commit may
name a person as author or co-author (`Co-authored-by: Name <email>`), or name
no one. It never attributes authorship or co-authorship to an AI assistant,
agent, bot, or other tool. A `commit-msg` hook in each repository and a shared
CI check enforce this; a person listed in the repository's `AUTHORS` or
`CONTRIBUTORS` file is always accepted, whatever their name.

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
