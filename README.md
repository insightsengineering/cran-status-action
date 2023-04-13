<!-- BEGIN_ACTION_DOC -->
# CRAN Status Check

### Description
Creates a summary of issues reported on the CRAN status check page for a given R package
### Action Type
Docker

### Inputs
* `package`:

  _Description_: Package name of the current R package deployed to CRAN


  _Required_: `true`

* `statuses`:

  _Description_: Create an issue if one or more of the following
statuses are reported on the check report.
This is a comma-separated string of statuses.
Allowed statuses are 'NOTE', 'WARN', and 'ERROR'


  _Required_: `false`

  _Default_: `ERROR`

### Outputs
None
<!-- END_ACTION_DOC -->
