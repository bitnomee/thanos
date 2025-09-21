# Testing Guide

This document outlines the testing strategy for this Helm chart.

## Overview

Testing ensures the quality and reliability of the chart. This chart follows the same testing principles as the original Bitnami Charts repository.

## Test Types

### Helm Template Tests
- Validate that templates render correctly
- Check that required values are properly validated
- Ensure resource names and labels are consistent

### Integration Tests
- Deploy the chart in a test environment
- Verify that all components start successfully
- Test basic functionality of the deployed application

## Running Tests Locally

### Prerequisites
- Kubernetes cluster (local or remote)
- Helm 3.8.0+
- kubectl configured to access your cluster

### Basic Chart Testing

1. **Lint the chart:**
   ```bash
   helm lint charts/thanos/
   ```

2. **Template validation:**
   ```bash
   helm template test-release charts/thanos/ --debug
   ```

3. **Install and test:**
   ```bash
   helm install test-release charts/thanos/
   helm test test-release
   ```

4. **Cleanup:**
   ```bash
   helm uninstall test-release
   ```

### Advanced Testing

For more comprehensive testing, you can:

1. Test with different values configurations
2. Test upgrades and rollbacks
3. Test in different Kubernetes environments
4. Validate security policies and resource limits

## Continuous Integration

This repository uses GitHub Actions for automated testing. The CI pipeline:

1. Lints the chart
2. Validates templates
3. Runs integration tests
4. Checks for security issues

## Test Configuration

Test configurations and parameters can be found in:
- `.vib/` directory (if migrated from original repo)
- Chart's `values.yaml` file for default configurations
- Custom test values in CI configuration

## Contributing Tests

When contributing changes:

1. Ensure existing tests pass
2. Add new tests for new features
3. Update test documentation as needed
4. Follow the same testing patterns used in the repository

## Test Acceptance Criteria

- Tests must be stateless and independent
- Tests must be retry-able and executable in any order
- Test scope should focus on chart installation and configuration
- Tests should be maintainable and use descriptive names
- Avoid hardcoded values where possible
