# PA2588 DevSecOps: Playground for Infrastructure as Code Security

This is part of the course DevSecOps.

> [!WARNING]
> This playground is not complete yet. Because you need to interact with AWS,
> this guide needs to be tested and adapted to work with the free tier.

## Preparation

  1. Click on [**Use this template**](https://github.com/new?template_name=pa2588-devsecops-iac-security&template_owner=bth-dipt-teaching)
     to create a new repository in your GitHub account (don't _fork_ it), and make sure to set the visibility to "Public".
  2. Go to "Settings" > "Secrets and variables" > "Actions"
  3. Create Repository Secrets `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY`

## Enable IaC Scanning with tfsec

  4. In `.github/workflows/tfsec.yml`, uncomment the block labeled "Version 1" to enable tfsec. 
     * After the next successful run of the GitHub actions, you should now see about a dozen of security issues being reported.
  5. In `iac/terraform.tfvars`, remove the existing `cidr` line and uncomment the "Version 2" block.
     * After the next successful run of the GitHub actions, you should now see two of the security issues being resolved.
