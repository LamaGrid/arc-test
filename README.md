# arc-test

A Rust hello world program with a GitHub Actions workflow that runs on a self-hosted ARC (Actions Runner Controller) scaling set.

## Building and Running

```bash
cargo build
cargo run
```

## GitHub Actions Workflow

The workflow in `.github/workflows/arc-demo.yml` runs on the `lama-arc-runner-set` self-hosted ARC runner scale set and can be triggered manually via `workflow_dispatch`.

```yaml
name: Actions Runner Controller Demo
on:
  workflow_dispatch:

jobs:
  Explore-GitHub-Actions:
    runs-on: lama-arc-runner-set
    steps:
    - run: echo "🎉 This job uses runner scale set runners!"
```
