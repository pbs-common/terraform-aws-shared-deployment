# terraform-aws-shared-deployment

Reusable Terraform modules shared by deployment repositories.

## Modules

- `backup`
- `ec2-workload`
- `managed-prefix-list`
- `mgn-organizations-delegation`
- `ssm-session-access-policy`

Each module is independently consumable from this repository using Terraform's Git
module source syntax:

```hcl
module "backup" {
  source = "git::https://github.com/pbs-common/terraform-aws-shared-deployment.git//modules/backup?ref=main"
}
```

For production promotion, replace `ref=main` with a release tag or commit
SHA after the corresponding shared-deployment change has been published.
