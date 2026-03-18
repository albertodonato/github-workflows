# Reusable GitHub workflows

This repository contains reusable workflows for GitHub.


## run-tox

Run a `tox` environment.

```yaml
jobs:
  test:
    name: Run tests
    uses: albertodonato/github-workflows/.github/workflows/run-tox.yaml@main
    with:
      python-version: "3.14"
      tox-env: test
```


## docker-build-publish

Build a docker image and publish it to GHCR.io and optionally to the Docker
Hub.

```yaml
jobs:
  build:
    name: Build and publish docker image
    uses: albertodonato/github-workflows/.github/workflows/docker-build-publish.yaml@main
    with:
      image-name: my-image
      dockerhub-image-name: my-image
      dockerhub-username: myuser
      suffix: bare
      platforms: linux/amd64,linux/arm64
    secrets: inherit

```

The image needs a `DOCKERHUB_TOKEN` set for Docker Hub access.
