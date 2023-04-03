The issue: Deleting a data factory component not working using CI CD pipelines

In the case that you are implementing CI CD for your Azure Data Factory you should have noticed that when you are deleting a resource like a pipeline or an activity from one environment (dev) and you commit, publish and merge, this change is not reflected in your other environment (QA, Prod). The reason is that CI CD can only merge changes, so it will not delete objects.

The good news is that you can enable this functionality using Azure DevOps and a PowerShell script that is provided by Microsoft. 

How this is done:

There are complete instructions on the steps to set up the run of the PowerShell script. 
Link [Continuous integration and delivery pre- and post-deployment scripts - Azure Data Factory | Microsoft Learn](https://learn.microsoft.com/en-us/azure/data-factory/continuous-integration-delivery-sample-script)

Link to the script: [Azure-DataFactory/PrePostDeploymentScript.Ver2.ps1 at main · Azure/Azure-DataFactory (github.com)](https://github.com/Azure/Azure-DataFactory/blob/main/SamplesV2/ContinuousIntegrationAndDelivery/PrePostDeploymentScript.Ver2.ps1)


