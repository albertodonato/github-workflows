# Reusable GitHub workflows

This repository contains reusable workflows for GitHub.


## pypi-release

Build a Python project and releases it to PyPI.

```yaml
jobs:
  test:
    name: Release
    uses: albertodonato/github-workflows/.github/workflows/pypi-release.yaml@main
    with:
      python-version: "3.14"
```


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
