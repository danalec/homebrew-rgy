# homebrew-rgy

A personal Homebrew **tap** for [rgy](https://github.com/danalec/rgy):
whole-filesystem name and content search in one stack.

This is NOT Homebrew/homebrew-core. The formula here is maintained by the
rgy project itself and installs the prebuilt macOS archives from the rgy
GitHub release; nothing is submitted to Homebrew's own repository.

## Install

```sh
brew tap danalec/rgy
brew install rgy-search
```

The tap name is `danalec/rgy` because Homebrew strips the `homebrew-`
prefix from `danalec/homebrew-rgy`.

## What it installs

`searchctl`, `searchd`, `rgy-autostart`, `rgxy`, and `rgy` (a symlink to
`searchctl`). Both Apple silicon and Intel Macs are supported, pinned to
the SHA256 of their release archives.

## Updating

The canonical formula lives in the rgy repository at
`Formula/rgy-search.rb`. On a new release, `scripts/publish-release.ps1`
rewrites its version and digests from the combined `SHA256SUMS`, and the
updated file is copied here. This tap is a distribution point, not a
second source of truth.