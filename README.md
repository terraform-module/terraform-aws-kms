# Terraform AWS KMS

[Terraform module](https://www.terraform.io/docs/providers/aws/r/kms_key.html) to create fully feature KMS

[![](https://img.shields.io/github/license/terraform-module/terraform-aws-kms)](https://github.com/terraform-module/terraform-aws-kms)
![](https://github.com/terraform-module/terraform-aws-kms/workflows/Labeler/badge.svg)
[![](https://img.shields.io/issues/github/terraform-module/terraform-aws-kms)](https://github.com/terraform-module/terraform-aws-kms)

## Usage example

Here's the gist of using it directly from github.

```hcl
module kms_chamber {
  source = "github.com/terraform-module/terraform-aws-kms.git?ref=v2.0.0"

  alias_name              = "parameter_store_key"
  description             = "Key to encrypt and decrypt secrets"

  tags = map("USED_BY", "chamber"))
}
```

## Assumptions

## Available features

## Module Variables

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| alias\_name | The name of the key alias | string | n/a | yes |
| deletion\_window\_in\_days | The duration in days after which the key is deleted after destruction of the resource | string | `"30"` | no |
| description | The description of this KMS key | string | n/a | yes |
| enable\_key\_rotation | \(Optional\) Specifies whether key rotation is enabled. Defaults to false. | bool | `"true"` | no |
| is\_enabled | \(Optional\) Specifies whether the key is enabled. Defaults to true. | bool | `"true"` | no |
| key\_policy | The policy of the key usage | string | `""` | no |
| tags | \(Optional\) A mapping of tags to assign to the object. | map | `{}` | no |

## Outputs

| Name | Description |
|------|-------------|
| key\_alias\_arn | The Amazon Resource Name \(ARN\) of the key alias |
| key\_alias\_name | The display name of the alias. |
| key\_arn | The Amazon Resource Name \(ARN\) of the key. |
| key\_id | The globally unique identifier for the key. |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

## Commands

<!-- START makefile-doc -->
```
$ make help
hooks                          Commit hooks setup
validate                       Validate with pre-commit hooks
changelog                      Update changelog
release                        Create release version
```
<!-- END makefile-doc -->


## License

Copyright 2019 ivankatliarhcuk

MIT Licensed. See [LICENSE](./LICENSE) for full details.

## How to Contribute

Submit a pull request

# Authors

Currently maintained by [Ivan Katliarchuk](https://github.com/ivankatliarchuk) and these [awesome contributors](https://github.com/terraform-module/terraform-aws-kms/graphs/contributors).