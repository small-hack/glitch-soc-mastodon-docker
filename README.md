# glitch-soc mastodon docker publishing repo
<a href="https://github.com/small-hack/glitch-soc-mastodon-docker/releases"><img src="https://img.shields.io/github/v/release/small-hack/glitch-soc-mastodon-docker?style=plastic&labelColor=484848&color=3CA324&logo=GitHub&logoColor=white"></a>[![](https://img.shields.io/docker/pulls/jessebot/mastodon-glitch-soc.svg)](https://cloud.docker.com/u/jessebot/repository/docker/jessebot/mastodon-glitch-soc)

A repo to publish the [glitch-soc/mastodon](https://github.com/glitch-soc/mastodon) docker container. glitch-soc is a fork of [mastodon](https://github.com/mastodon/mastodon) Learn more about it [here](https://glitch-soc.github.io/docs/).

## How this repo works

The [`docker-push-daily.yml`](./github/workflows/docker-push-daily.yml) GitHub Actions Workflow will:
- clone the [glitch-soc](https://github.com/glitch-soc/mastodon)
- get the latest GitHub Release of glitch-soc
- builds the docker image and pushes it up as [jessebot/mastodon-glitch-soc](https://cloud.docker.com/u/jessebot/repository/docker/jessebot/mastodon-glitch-soc)
- creates a release on this repo with with the current docker version built
