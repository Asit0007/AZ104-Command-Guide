# AZ104-Command-Guide

## Description
This repository serves as a comprehensive guide to essential Azure PowerShell and Azure CLI commands for the AZ-104 Microsoft Azure Administrator certification. The commands cover core topics like subscription management, resource management, and Active Directory, and provide key points to remember specifically for the AZ-104 exam.

---

## Azure Subscription Management and Resource Commands

### Subscription Management Commands

| Task                                 | PowerShell Command                                         | Azure CLI Command                           |
|--------------------------------------|------------------------------------------------------------|---------------------------------------------|
| **List Subscriptions**               | `Get-AzSubscription`                                       | `az account list`                           |
| **Set Active Subscription**          | `Select-AzSubscription -SubscriptionId <ID>`               | `az account set --subscription <ID>`        |
| **Show Current Context**             | `Get-AzContext`                                            | `az account show`                           |
| **List All Accounts**                | `Get-AzAccount`                                            | `az account list --output table`           |
| **Get Role Assignments**             | `Get-AzRoleAssignment -Scope <Scope>`                      | `az role assignment list --scope <Scope>`   |

### Resource Management Commands

| Task                                  | PowerShell Command                                         | Azure CLI Command                                   |
|---------------------------------------|------------------------------------------------------------|-----------------------------------------------------|
| **Authenticate Account**              | `Connect-AzAccount`                                        | `az login`                                          |
| **List Resource Groups**              | `Get-AzResourceGroup`                                      | `az group list --output table`                      |
| **Create Resource Group**             | `New-AzResourceGroup -Name <Name> -Location <Location>`    | `az group create --name <Name> --location <Location>` |
| **List Virtual Machines**             | `Get-AzVM`                                                 | `az vm list --output table`                         |
| **Start Virtual Machine**             | `Start-AzVM -Name <VMName> -ResourceGroupName <ResourceGroup>` | `az vm start --name <VMName> --resource-group <ResourceGroup>` |
| **Stop Virtual Machine**              | `Stop-AzVM -Name <VMName> -ResourceGroupName <ResourceGroup>` | `az vm stop --name <VMName> --resource-group <ResourceGroup>` |
| **Delete Resource Group**             | `Remove-AzResourceGroup -Name <Name>`                      | `az group delete --name <Name> --yes --no-wait`     |
| **List Storage Accounts**             | `Get-AzStorageAccount`                                     | `az storage account list --output table`            |
| **Create Storage Account**            | `New-AzStorageAccount -Name <Name> -ResourceGroupName <ResourceGroup> -Location <Location> -Sku <SkuType>` | `az storage account create --name <Name> --resource-group <ResourceGroup> --location <Location> --sku <SkuType>` |
| **List AD Users**                     | `Get-AzADUser`                                             | `az ad user list --output table`                    |

---

### Key Points for AZ-104 Exam

#### Subscription Management Commands
1. **Get-AzSubscription / az account list**: Useful for tracking all subscriptions and organizing billing/resource access.
2. **Select-AzSubscription / az account set**: Ensures that all subsequent actions apply to the correct subscription.
3. **Get-AzContext / az account show**: Important for verifying the active subscription before running commands.
4. **Get-AzAccount / az account list**: Helps confirm all accessible subscriptions across accounts.
5. **Get-AzRoleAssignment / az role assignment list**: Useful for role-based access control and security compliance.

#### Resource Management Commands
1. **Connect-AzAccount / az login**: First command to start any Azure session.
2. **Get-AzResourceGroup / az group list**: Essential for organizing resources and viewing all resource groups.
3. **New-AzResourceGroup / az group create**: Creates logical resource containers, ensuring resources are managed by location.
4. **Get-AzVM / az vm list**: Key for viewing the status and details of VMs.
5. **Start-AzVM / az vm start**: Commonly used to start compute resources; remember it for cost management.
6. **Stop-AzVM / az vm stop**: Stops (deallocates) a VM to reduce costs but retains its configuration.
7. **Remove-AzResourceGroup / az group delete**: Important for cleanup and managing costs.
8. **Get-AzStorageAccount / az storage account list**: Useful for checking all storage accounts across subscriptions.
9. **New-AzStorageAccount / az storage account create**: Familiarize yourself with SKU types for performance/cost optimization.
10. **Get-AzADUser / az ad user list**: Important for managing Azure AD users and permissions.

---

This guide provides a quick, exam-focused reference to help you prepare for the AZ-104 exam. Be sure to practice each command to reinforce your understanding and readiness.
