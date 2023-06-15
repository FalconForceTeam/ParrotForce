# ParrotForce
Azure playbook for automatic evidence collection through MDE

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

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/)

Fill in the details of your deployment

## Manual Deployment
1. Login to [Azure Portal](https://portal.azure.com)
2. In the top bar search for "template" and select `Deploy a custom template` to start the deployment
![Alt text](4.Azure.png)
3. Select the `Build your own template in the editor` to manually import ParrotForce
![Alt text](5.Deploy.png)
4. Click `Load File` and select the `deployazure.json` file to deploy ParrotForce
![Alt text](6.Template.png)
5. Click Save and assign ParrotForce to your Resource Group and Subscription of your choice.

## Screenshots
