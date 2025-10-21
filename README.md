# CLI GitHub Action

A GitHub Action that downloads the TangleGuard CLI tool and executes the `validation-all` command on the checkout repository.

## Features

- Automatically checks out your repository
- Downloads TangleGuard CLI
- Makes downloaded tools executable
- Runs validation command
- Fails when architecture drift is detected

## Usage

### Basic Example

```yaml
name: Run CLI Tool
on: [push]

jobs:
  run-cli:
    runs-on: ubuntu-latest
    steps:
      - name: TangleGuardRun CLI tool
        uses: ./
```

## License

This GitHub Action is licensed under the MIT License.

However, this action downloads and uses TangleGuard CLI, which is a proprietary software with its own license terms.
