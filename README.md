# Do Tofu or Terraform

<!-- action-docs-all source="action.yml" project="jamcatbiz/do-tf" version="x.x.x" -->
## Description

Assists in running various tf workflows from GitHub Actions.

## Inputs

| name | description | required | default |
| --- | --- | --- | --- |
| `tf_flavor` | <p>Which flavor of tf infra-as-code to use; <code>tofu</code> or <code>terraform</code></p> | `true` | `""` |
| `dir_path` | <p>Path relative to root of repo for working tf dir.</p> | `true` | `""` |
| `version` | <p>Version of the tf executable to install.</p> | `true` | `""` |
| `plan_only` | <p>Boolean for whether to only plan and not apply.</p> | `true` | `""` |
| `init_args` | <p>[Optional] Additional command line args. Useful for --backend-config and ephemeral or dynamic deploys.</p> | `false` | `""` |
| `plan_args` | <p>[Optional] Additional command line args. Useful for --var-file and ephemeral or dynamic deploys.</p> | `false` | `""` |
| `plan_artifact_name` | <p>[Optional] Artifact name for plan file to use. If passed, then we jump straight to apply.</p> | `false` | `""` |


## Outputs

| name | description |
| --- | --- |
| `tf_output` | <p>tf outputs in -json format.</p> |
| `plan_artifact_name` | <p>Name of the relevant tf plan artifact, either produced, consumed, or both.</p> |


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

    version:
    # Version of the tf executable to install.
    #
    # Required: true
    # Default: ""

    plan_only:
    # Boolean for whether to only plan and not apply.
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