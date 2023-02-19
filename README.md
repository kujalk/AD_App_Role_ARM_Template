# Deploying Custom Role Definition and Role Assignment with Azure ARM Template
This is an Azure ARM template that can be used to deploy a custom role definition and role assignment to an Azure subscription or resource group.

## How to Use
To use this template, follow these steps:

1. Clone or download the repository to your local machine.

2. Open the `ARM_Template.json` file in a text editor or integrated development environment (IDE).

3. Customize the parameter values as needed, including the roleName, AppName, roleNameGuid, and roleAssignmentGuid.

4. Save the azuredeploy.json file.

5. Open the Azure Portal and navigate to the subscription or resource group where you want to deploy the custom role definition and role assignment.
6. Click on "Deploy a custom template" and select the azuredeploy.json file from your local machine.

7.Follow the prompts to complete the deployment process.

## Parameters
This ARM template has the following parameters:

. `roleName`: The name of the custom role.

. `AppName`: The Azure App name.

. `roleNameGuid`: A new GUID used to identify the role definition resource.

. `roleAssignmentGuid`: A new GUID used to identify the role assignment resource.

## Resources
This ARM template creates the following resources:

`Microsoft.Resources/deploymentScripts`: A deployment script that runs a PowerShell command to retrieve the service principal ID for the specified Azure App.

`Microsoft.Authorization/roleDefinitions`: A custom role definition that grants read permissions.

`Microsoft.Authorization/roleAssignments`: A role assignment that assigns the custom role to the service principal ID retrieved by the deployment script.


## Conclusion
This Azure ARM template provides a quick and easy way to deploy a custom role definition and role assignment to an Azure subscription or resource group. By using this template, users can ensure that their custom roles are deployed in a consistent and repeatable manner, while maintaining a high level of flexibility and control.
