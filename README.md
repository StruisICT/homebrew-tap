# homebrew-tap

[Homebrew](https://brew.sh) tap for **StruisICT** tools.

## Use

```sh
brew tap struis112/tap
brew install smtp-test-tool
brew upgrade smtp-test-tool   # picks up new versions automatically
```

Works on macOS (Apple Silicon + Intel) and Linux x86_64.

## Formulae

| Formula | Source repo | License |
|---------|-------------|---------|
| [`smtp-test-tool`](Formula/smtp-test-tool.rb) | [Struis112/smtp-test-tool](https://github.com/Struis112/smtp-test-tool) | MIT OR Apache-2.0 |

## How updates happen

`smtp-test-tool`'s release workflow rewrites
[`packaging/homebrew/smtp-test-tool.rb`](https://github.com/Struis112/smtp-test-tool/blob/main/packaging/homebrew/smtp-test-tool.rb)
on every published version, with the new version numbers and SHA-256
hashes for each platform.  This tap is a *mirror* of that file - keep
them in sync by running, from the smtp-test-tool repo root:

```sh
cp packaging/homebrew/smtp-test-tool.rb ../homebrew-tap/Formula/smtp-test-tool.rb
cd ../homebrew-tap
git add Formula && git commit -m "smtp-test-tool: $(grep '^  version' Formula/smtp-test-tool.rb | cut -d'\"' -f2)" && git push
```

## License

The formulae in this repo are CC0 / public domain.  The tools they
install carry their own licenses (visible in each formula's `license`
field).
