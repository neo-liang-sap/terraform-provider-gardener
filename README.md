
# Terraform Provider for Gardener

- Website: https://www.terraform.io

## Overview
Creating a new Terraform provider for Gardener using the Gardener client.

## Prerequisites
- [Terraform CLI](https://www.terraform.io/downloads.html)

## Installation
This PoC contains a terraform provider that is meant to be executed by the terraform CLI. In order to runn it:
1. Resolve dependencies:
    ```bash
    dep ensure
    ```
2. Build the provider:
    ```bash
    go build -o terraform-provider-gardener
    ```
3. Edit the `example.tf` file providing the required gardener configuration:
    - Gardener project name
    - Gardener secret for the choosen cloud provider(s).
    - Path to the gardener kubeconfig.
    > NOTE: To obtain gardener configurations visit the gardener dashboard
4. Initialise terraform:
    ```bash
    terraform init
    ```
5. Plan the provisioning:
    ```bash
    terraform plan
    ```
6. Deploy the cluster:
    ```bash
    terraform apply
    ```
