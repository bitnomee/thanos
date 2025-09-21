# Contributing Guidelines

Contributions are welcome via GitHub Pull Requests. This document outlines the process to help get your contribution accepted.

## How to Contribute

1. Fork this repository, develop, and test your changes.
2. Submit a pull request.

### Technical Requirements

When submitting a PR make sure that it:

- Must pass CI jobs for linting and testing.
- Must follow [Helm best practices](https://helm.sh/docs/chart_best_practices/).
- Any change to the chart requires a version bump following [semver](https://semver.org/) principles.
- Any change to a Helm template must include a license header like the following:

```yaml
{{- /*
Copyright Broadcom, Inc. All Rights Reserved.
SPDX-License-Identifier: APACHE-2.0
*/}}
```

#### Sign Your Work

The sign-off is a simple line at the end of the explanation for a commit. All commits need to be signed. Your signature certifies that you wrote the patch or otherwise have the right to contribute the material.

Then you just add a line to every git commit message:

```text
Signed-off-by: Joe Smith <joe.smith@example.com>
```

Use your real name (sorry, no pseudonyms or anonymous contributions.)

If you set your `user.name` and `user.email` git configs, you can sign your commit automatically with `git commit -s`.

### Documentation Requirements

- The chart's `README.md` must include configuration options.
- The chart's `NOTES.txt` must include relevant post-installation information.
- The title of the PR should start with the chart name.

### Testing

Please ensure your changes pass the existing tests and add new tests as appropriate for your changes.

## Development Setup

1. Fork and clone this repository
2. Make your changes in the `charts/thanos/` directory
3. Test your changes locally
4. Submit a pull request

## Chart Structure

This repository contains a single Helm chart located in `charts/thanos/`. The chart follows the same structure and conventions as the original Bitnami Charts.

## License

By contributing to this project, you agree that your contributions will be licensed under the Apache License 2.0.
