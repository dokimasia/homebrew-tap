<!--
  ~ Copyright Dokimasia B.V. 2026
  ~ SPDX-License-Identifier: MIT
-->

# Dokimasia Tap

The Homebrew casks of the commands that Dokimasia releases. The release workflow of each command commits its cask, so do not edit a cask by hand: the next release of its command overwrites it.

## Install a cask

```sh
brew install --cask dokimasia/tap/ergon
```

To tap the repository once and then install a cask by its name:

```sh
brew tap dokimasia/tap
brew install --cask ergon
```

In a `Brewfile`:

```ruby
tap "dokimasia/tap"
cask "ergon"
```

## Casks

| Cask | Command | Repository |
|---|---|---|
| `ergon` | Sets up a repository with a managed baseline, and releases its packages | [dokimasia/ergon](https://github.com/dokimasia/ergon) |

A cask installs the release archive of its command for macOS or Linux, and checks the archive against the SHA-256 that the cask states. It also installs the completions of bash, zsh and fish. The binaries are not notarized, so the cask removes the quarantine attribute on macOS.

## Updates

After each release of a command, the job `homebrew` of its release workflow commits `Casks/<name>.rb` with a token of the GitHub App of Dokimasia. `brew test-bot` checks the style and the syntax of every cask on each push and pull request.

## Documentation

`brew help`, `man brew` or [Homebrew's documentation](https://docs.brew.sh).
