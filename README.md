# Thanos Helm Chart

## Migrated from Bitnami Charts

This is the Thanos Helm chart migrated from the [Bitnami Charts](https://github.com/bitnami/charts) repository.

Git history relevant to this chart was maintained, as well as tags.

In order for it to be functional, `charts/thanos/` will need the following updates:

- Defaults update so that images are not pulled from bitnami. Instead, they should ideally be pulled
  from the upstream project's official registry
- Github action worklflows configured to run tests
- Release automation enabled to publish to GHCR
- `CODE_OF_CONDUCT.md`, `CONTRIBUTING.md`, `SECURITY.md`, and `TESTING.md` reviewed and updated if necessary
- READMEs updates appropriately

## Installation

```bash
helm install RELEASE_NAME oci://ghcr.io/bitrot-charts/chart-thanos
```

## Configuration

See [charts/thanos/values.yaml](./charts/thanos/values.yaml) for configuration options.

## Development

This repository follows the same development practices as the original Bitnami Charts. Please see:

- [Contributing Guidelines](./CONTRIBUTING.md)
- [Testing Guide](./TESTING.md)
- [Code of Conduct](./CODE_OF_CONDUCT.md)

## Source

This chart was migrated from [`bitnami/thanos`](https://github.com/bitnami/charts/tree/main/bitnami/thanos) with full git history preserved.

## License

This chart is licensed under the Apache License 2.0. See the [LICENSE](./LICENSE) file for details.
