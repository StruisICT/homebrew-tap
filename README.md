# homebrew-tap

[Homebrew](https://brew.sh) tap for **StruisICT** tools.

## Use

```sh
brew tap struisict/tap

# CLI tool (macOS + Linux)
brew install smtp-test-tool

# GUI app (macOS only)
brew install --cask inlook

# Picks up new versions automatically
brew upgrade
```

Formulae work on macOS (Apple Silicon + Intel) and Linux x86_64.
Casks are macOS-only.

## Formulae

| Formula | Source repo | License |
|---------|-------------|---------|
| [`smtp-test-tool`](Formula/smtp-test-tool.rb) | [Struis112/smtp-test-tool](https://github.com/Struis112/smtp-test-tool) | MIT OR Apache-2.0 |

## Casks

| Cask | Source repo | License |
|------|-------------|---------|
| [`inlook`](Casks/inlook.rb) | [StruisICT/InLook](https://github.com/StruisICT/InLook) | MIT OR Apache-2.0 |

## How updates happen

Each source repo's release workflow rewrites its `packaging/homebrew/<name>.rb`
file on every published version, with the new version numbers and SHA-256
hashes for each platform. This tap is a *mirror* of those files - keep them
in sync by running, from the source repo root:

```sh
# Formulae
cp packaging/homebrew/smtp-test-tool.rb ../homebrew-tap/Formula/smtp-test-tool.rb

# Casks
cp packaging/homebrew/inlook.rb ../homebrew-tap/Casks/inlook.rb

cd ../homebrew-tap
git add Formula Casks && git commit -m "<name>: <version>" && git push
```

## License

The formulae and casks in this repo are CC0 / public domain. The tools they
install carry their own licenses (visible in each file's `license` field
or upstream).
