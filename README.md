<!-- BEGIN_ACTION_DOC -->
# CRAN Status Monitor

### Description

Creates a summary of issues reported on the CRAN status check page for a given R package.

### Action Type

Composite.

### Inputs

* `statuses`:

  _Description_: Create an issue if one or more of the following
statuses are reported on the check report.
This is a comma-separated string of statuses.
Allowed statuses are 'NOTE', 'WARN', and 'ERROR'

  _Required_: `false`

  _Default_: `ERROR`

* `issue-assignees`:

  _Description_: To whom should the issue be assigned to if errors are
encountered in the CRAN status checks?
This is a comma-separated string of GitHub usernames.
If undefined or empty, no assignments are made.

  _Required_: `false`

  _Default_: `''`

* `path`:

  _Description_: Path to the R package root, if the package is not at the
      top level of the repository.

  _Required_: `false`

  _Default_: `.`

### Outputs

None
<!-- END_ACTION_DOC -->

### Example usage:

```yaml
jobs:
  cran-status:
    name: Check Status
    runs-on: ubuntu-latest
    container:
      image: rocker/tidyverse:latest
    steps:
      - name: Run CRAN Status Action
        uses: insightsengineering/cran-status-action@main
        with:
          statuses: "ERROR"
          issue-assignees: "username1"
```

We acknowledge that a similar action, based on code from [pharmaverse/admiralci](https://github.com/pharmaverse/admiralci) repository, has been created: https://github.com/dieghernan/cran-status-check.

The action contained in this repository is simply our take on how to perform the CRAN status check 😄
