# Woodpecker-windows

[![pipeline-status](https://ci.geco-it.net/api/badges/woodpecker/woodpecker-windows/status.svg)](https://ci.geco-it.net/repos/woodpecker/woodpecker-windows)
[![issues](https://git.geco-it.net/woodpecker/woodpecker-windows.git/badges/issues/open.svg?logo=forgejo&label=Issues&color=red)](https://git.geco-it.net/woodpecker/woodpecker-windows.git/issues?state=open)
[![pulls](https://git.geco-it.net/woodpecker/woodpecker-windows.git/badges/pulls/open.svg?logo=forgejo&label=Pulls&color=orange)](https://git.geco-it.net/woodpecker/woodpecker-windows.git/pulls?state=open)
[![release](https://git.geco-it.net/woodpecker/woodpecker-windows.git/badges/release.svg?logo=forgejo&label=Release)](https://git.geco-it.net/woodpecker/woodpecker-windows.git/releases)
[![license](https://img.shields.io/badge/License-GPLv3-blue)](./LICENSE)

> **Warning**
> Read-only source code mirror of Geco-iT Open Source projects.

All stuff for use [Woodpecker CI](https://woodpecker-ci.org) on Windows

- [Woodpecker-windows](#woodpecker-windows)
  - [Install Woodpecker Agent](#install-woodpecker-agent)
    - [Docker Backend](#docker-backend)
    - [Local Backend](#local-backend)
  - [Pipeline Usage](#pipeline-usage)
    - [Backend Docker](#backend-docker)
    - [Backend Local](#backend-local)
  - [Plugins Usage](#plugins-usage)
  - [License](#license)
  - [Author Information](#author-information)

## Install Woodpecker Agent

### Docker Backend

Follow [documentation](./agent/backend-docker/README.md)

### Local Backend

Follow [documentation](./agent/backend-local/README.md)

## Pipeline Usage

### Backend Docker

```yaml
---
labels:
  platform: windows/amd64
  backend: docker

workspace:
  base: C:\src

clone:
  git:
    # $ docker image tag \
    #        <REPO_URL>/woodpecker/woodpecker-git-plugin:latest \
    #        woodpeckerci/plugin-git:latest
    image: woodpeckerci/plugin-git
    pull: false

steps:
...
```

### Backend Local

```yaml
---
labels:
  platform: windows/amd64
  backend: local

steps:
...
```

## Plugins Usage

- [git](./plugins/plugin-git/README.md)
- [drone-docker](./plugins/plugin-drone-docker/README.md)
- [drone-s3](./plugins/plugin-drone-s3/README.md)

## License

Released under GPLv3+

## Author Information

This Windows port was created in 2024 by Cyril DUCHENOY, CEO of [Geco-iT SARL](https://www.geco-it.fr).
