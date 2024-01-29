# Azure Container Instance Terraform Configuration

This Terraform configuration deploys an Azure Container Instance (ACI) with specified parameters. It creates a resource group and an ACI containing a single container based on the provided Docker image.

## Prerequisites

Before you begin, ensure you have the following:

1. [Terraform](https://www.terraform.io/) installed on your machine.
2. Azure CLI installed and authenticated.

## Configuration

### Variables

The configuration is driven by variables defined in the `variables.tf` file. Here are the configurable variables:

- **location**: Azure region for resource deployment.
- **rgname**: Name of the Azure Resource Group.
- **container_group_name**: Name of the Azure Container Group.
- **container_name**: Name of the container within the Container Group.
- **image**: Docker image for the container.
- **port**: Port to expose on the container.
- **cpu**: Number of CPU cores allocated to the container.
- **memory**: Amount of memory allocated to the container in gigabytes.
- **restart_policy**: Restart policy for the container.
- **iptype**: IP address type for the container (Private or Public).
- **ostype**: Operating system type for the container (Windows or Linux).
- **prot**: Protocol for the exposed port (TCP or UDP).

### Terraform Variables File (terraform.tfvars)

Make sure to update `terraform.tfvars` file according to your requirements.

## Usage
### 1. Initialize Terraform:
`terraform init`
### 2. Review the execution plan:
`terraform plan`
### 3. Apply the changes:
`terraform apply`

Confirm by typing **yes** when prompted.

## Clean Up
To avoid incurring charges, it's recommended to destroy the resources when they are no longer needed.<br>

`terraform destroy`

Confirm by typing **yes** when prompted.

## Note
- Ensure that your Azure CLI is authenticated and configured with the correct subscription before running Terraform commands.

- Make sure you have proper permissions in Azure to create and manage resources.

- Review and customize the variables in the terraform.tfvars file based on your requirements.
