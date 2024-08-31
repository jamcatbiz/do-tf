# Do Tofu

<!-- action-docs-all source="action.yml" project="jamcatbiz/do-tf" version="x.x.x" -->
## Description

Assists in running various tf workflows from GitHub Actions.

## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `tf_flavor` | <p>Which flavor of tf infra-as-code to use; <code>tofu</code> or <code>terraform</code></p> | `true` | `""` |
| `dir_path` | <p>Path relative to root of repo for working tf dir.</p> | `true` | `""` |
| `vars` | <p>Path relative to working tf dir for <code>.tfvars</code> file.</p> | `true` | `""` |
| `backend` | <p>Path relative to working tf dir for <code>.tfbackend</code> file.</p> | `true` | `""` |
| `version` | <p>Version of the tf executable to install.</p> | `true` | `""` |
| `plan_only` | <p>Boolean for whether to only plan and not apply/destroy, default false</p> | `true` | `""` |
| `destroy` | <p>Boolean for whether to destroy or not, default false, meaning this action will apply by default.</p> | `true` | `""` |
| `init_args` | <p>[Optional] Additional command line args. Useful for --backend-config and ephemeral or dynamic deploys.</p> | `false` | `""` |
| `plan_args` | <p>[Optional] Additional command line args. Useful for --var-file and ephemeral or dynamic deploys.</p> | `false` | `""` |
| `plan_artifact_name` | <p>[Optional] Artifact name for plan file to use. If passed, then we jump straight to apply.</p> | `false` | `""` |


## Outputs

| name | description |
| --- | --- |
| `output` | <p>tf outputs in -json format.</p> |


## Runs

This action is a `composite` action.

## Usage

```yaml
- uses: jamcatbiz/do-tf@x.x.x
  with:
    tf_flavor:
    # Which flavor of tf infra-as-code to use; `tofu` or `terraform`
    #
    # Required: true
    # Default: ""

    dir_path:
    # Path relative to root of repo for working tf dir.
    #
    # Required: true
    # Default: ""

    vars:
    # Path relative to working tf dir for `.tfvars` file.
    #
    # Required: true
    # Default: ""

    backend:
    # Path relative to working tf dir for `.tfbackend` file.
    #
    # Required: true
    # Default: ""

    version:
    # Version of the tf executable to install.
    #
    # Required: true
    # Default: ""

    plan_only:
    # Boolean for whether to only plan and not apply/destroy, default false
    #
    # Required: true
    # Default: ""

    destroy:
    # Boolean for whether to destroy or not, default false, meaning this action will apply by default.
    #
    # Required: true
    # Default: ""

    init_args:
    # [Optional] Additional command line args. Useful for --backend-config and ephemeral or dynamic deploys.
    #
    # Required: false
    # Default: ""

    plan_args:
    # [Optional] Additional command line args. Useful for --var-file and ephemeral or dynamic deploys.
    #
    # Required: false
    # Default: ""

    plan_artifact_name:
    # [Optional] Artifact name for plan file to use. If passed, then we jump straight to apply.
    #
    # Required: false
    # Default: ""
```
<!-- action-docs-all source="action.yml" project="jamcatbiz/do-tf" version="x.x.x" -->