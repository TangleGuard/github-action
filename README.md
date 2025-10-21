# TangleGuard CLI GitHub Action

A GitHub Action that installs the TangleGuard CLI and validates interdependencies within a codebase regarding user defined rules.

The allowed dependencies are declared in `tangleguard.json` and is configurable via the TangleGuard Designer.

More information can be found at https://docs.tangleguard.com/

## Procedure

- Checks out your repository
- Downloads TangleGuard CLI and makes it executable
- Runs validation command
- Fails when architecture drift (dependency rule violations) are detected

## Usage

### Basic Example

```yaml
name: Architecture Check
on: [push, pull_request]

jobs:
  validate-architecture:
    runs-on: ubuntu-latest
    steps:
      - uses: TangleGuard/github-action@main
```

## License

This GitHub Action is licensed under the MIT License.

However, this action downloads and uses TangleGuard CLI, which is a proprietary software with its own license terms.
