# 🦜ParrotForce
Azure playbook for automatic evidence collection.

Current playbook only includes MDE live response for Windows systems.

## Prerequisites
ParrotForce uses connections to Azure Sentinel and Microsoft 365 Defender to function. The following API permissions need to be present in your managed identity that connects to Azure Sentinel and Microsoft 365 Defender:
- AdvancedQuery.Read.All
- Alert.Read.All
- File.Read.All
- Machine.CollectForensics
- Machine.LiveResponse

By default, the Logic App of the template is configured on “Consumption” plan type, hence pricing will only occur upon workflow execution.

## Quick Deployment
Click on the button to deploy automatically to your Azure Subscription

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FFalconForceTeam%2FParrotForce%2Fmain%2Fazuredeploy.json)

## Manual Deployment
1. Login to [Azure Portal](https://portal.azure.com)
2. In the top bar search for "template" and select `Deploy a custom template` to start the deployment
3. Select the `Build your own template in the editor` to manually import ParrotForce
4. Click `Load File` and select the `deployazure.json` file to deploy ParrotForce
5. Click Save and assign ParrotForce to your Resource Group and Subscription of your choice.

## Sentinel Repository (CI/CD)
1. Add folder to your repository
2. Revalidate all connections, Sentinel, MDATP for all corresponding blocks. It's advised to use managed identity as much as possible.

## All deployments
1. Upload needed files inside MDATP/MDE library (typically make a live response session). By default: trident.ps1, winpmem.exe.
  * https://github.com/nov3mb3r/trident (ps1 not signed by default)
  * https://github.com/Velocidex/WinPmem
