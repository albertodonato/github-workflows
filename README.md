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
