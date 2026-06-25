<h1 align="center">Gitlab Sync<br />
<div align="center">
  
  [![Build](https://github.com/action-pack/gitlab-sync/workflows/Build/badge.svg)](https://github.com/action-pack/gitlab-sync/)
  [![Version](https://img.shields.io/github/v/tag/action-pack/gitlab-sync?label=version&sort=semver&color=066da5)](https://github.com/marketplace/actions/gitlab-sync)
  [![Size](https://img.shields.io/github/languages/code-size/action-pack/gitlab-sync?label=size&color=066da5)](https://github.com/action-pack/gitlab-sync/)
  
</div></h1>

Action to mirror a repository to GitLab.

## Usage 🚀

```yaml
name: Gitlab Sync

on: [push, pull_request, create, delete]

jobs:
  sync:
    name: Gitlab Sync
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
        with:
          fetch-depth: 0
      - uses: action-pack/gitlab-sync@v3
        with:
          username: ${{ github.actor }}
          url: https://gitlab.com/${{ github.repository }}.git
          # Personal access token from gitlab.com 
          token: ${{ secrets.GITLAB_TOKEN }}
```

## Stars 🌟
![Stargazers](https://raw.githubusercontent.com/star-stats/stars/refs/heads/data/charts/action-pack-gitlab-sync.svg)
