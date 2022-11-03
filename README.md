# GitHub Action: Pre-Commit

- Installs Python
- Caches pre-commit enviroment
- Runs `pre-commit`

## Usage

<!-- action-docs-inputs -->

### Inputs

| parameter  | description                             | required | default     |
| ---------- | --------------------------------------- | -------- | ----------- |
| extra_args | options to pass to pre-commit run       | `true`   | --all-files |
| ssh-key    | SSH key to access private repositories. | `false`  |             |

<!-- action-docs-inputs -->

<!-- action-docs-outputs -->

<!-- action-docs-outputs -->

## Example

```yaml
jobs:
  pre-commit:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: digitalr00ts/action-pre-commit@trunk
```
