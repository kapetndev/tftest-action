# tftest-action

GitHub Action to download and execute `tftest` for Terraform testing.

## Usage

```yaml
- name: Run tftest
  uses: kapetndev/tftest-action@v1.0.0
  with:
    additional_args: --out tftest-results.json
    format: json
    version: 1.0.0
    terraform_version: 1.5.0
    working_directory: ./modules
```

## Inputs

| Name | Description | Default | Required |
|------|-------------|---------|:--------:|
| `additional-args` | Additional argument to `tftest` | - | no |
| `format` | Output format: `text`, `json`, or `prettyjson` | `json` | no |
| `terraform-version` | Version of Terraform to use | `latest` | no |
| `version` | Version of tftest to use | `latest` | no |
| `working-directory` | Base path from which to start testing | `.` | no |

## Outputs

| Name | Description |
|------|-------------|
| `tftest-return-code` | Output from tftest execution |

## License

This project is licensed under the [MIT License](LICENSE).
