# Check code formatting for ModOrganizer repositories

Action to check code formatting for ModOrganizer 2 components within Github workflows.

**Example usage**:

```yml
name: Lint Mob

on:
  push:
  pull_request:
    types: [opened, synchronize, reopened]

jobs:
  lint:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Check format
        uses: ModOrganizer2/check-formatting-action@master
        with:
          check-path: "."
          exclude-regex: "third-party"
```

## Configuration

See https://github.com/jidicula/clang-format-action.
