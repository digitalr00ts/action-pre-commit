# GitHub Action: Pre-Commit

- Installs Python
- Caches pre-commit enviroment
- Runs `pre-commit`

## Usage

### Inputs

| label           | default     | required | description                             |
| --------------- | ----------- | -------- | --------------------------------------- |
| python-version  |             | Yes      | The Python version to use.              |
| skip-py-install | false       | No       | Skip installing Python.                 |
| extra-args      | --all-files | Yes      | Options to pass to pre-commit.          |
| ssh-private-key |             | No       | SSH key to access private repositories. |

## Example

```yaml
jobs:
  pre-commit:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: digitalr00ts/action-pre-commit@trunk
```
