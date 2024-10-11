# golangci-lint


- [License](https://github.com/golangci/golangci-lint/blob/master/LICENSE)
- [Release](https://github.com/golangci/golangci-lint/releases/latest)
- [Docker](https://hub.docker.com/r/golangci/golangci-lint)
- [GitHub Releases Stats of golangci-lint](https://somsubhra.github.io/github-release-stats/?username=golangci&repository=golangci-lint)

`golangci-lint` is a fast linters runner for Go.

It runs linters in parallel, uses caching, supports YAML configuration,
integrates with all major IDEs, and includes over a hundred linters.

Join our slack channel by [joining Gophers workspace](https://invite.slack.golangbridge.org/)
and then [joining](https://gophers.slack.com/archives/CS0TBRKPC) channel [`#golangci-lint`](https://gophers.slack.com/archives/CS0TBRKPC).

Follow the news and releases:

- [Follow on Mastodon](https://fosstodon.org/@golangcilint)
- [Follow on Twitter](https://twitter.com/golangci)

## Features

- ⚡ [Very fast](https://golangci-lint.run/product/performance): runs linters in parallel, reuses Go build cache and caches analysis results.
- ⚙️ YAML-based [configuration](https://golangci-lint.run/usage/configuration).
- 🖥 [Integrations](https://golangci-lint.run/welcome/integrations) with VS Code, Sublime Text, GoLand, GNU Emacs, Vim, GitHub Actions.
- 🥇 [A lot of linters](https://golangci-lint.run/usage/linters) included, no need to install them.
- 📈 Minimum number of [false positives](https://golangci-lint.run/usage/false-positives) because of tuned default settings.
- 🔥 Nice output with colors, source code lines and marked `identifiers`.

[Get started now!](https://golangci-lint.run/welcome/install)

### Docker

```sh
docker run --rm -v $(pwd):/app -w /app golangci/golangci-lint:{.LatestVersion} golangci-lint run -v
```

Preserving cache between consecutive runs:
```sh
docker run --rm -v $(pwd):/app -v ~/.cache/golangci-lint/{.LatestVersion}:/root/.cache -w /app golangci/golangci-lint:{.LatestVersion} golangci-lint run -v
```

Colored output:
```sh
docker run -t --rm -v $(pwd):/app -w /app golangci/golangci-lint:{.LatestVersion} golangci-lint run -v
```

## Supporting Us

- [Open Collective backers and sponsors](https://opencollective.com/golangci-lint)
- [GitHub Sponsors](https://github.com/sponsors/golangci)
- [Linter Authors](https://golangci-lint.run/product/thanks/)

`golangci-lint` is a free and open-source project built by volunteers.

If you value it, consider supporting us, we appreciate it! ❤️
