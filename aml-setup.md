## Before you start

You'll need an [Azure subscription](https://azure.microsoft.com/free?azure-portal=true) in which you have administrative-level access.

## Provision an Azure Machine Learning workspace

An Azure Machine Learning *workspace* provides a central place for managing all resources and assets you need to train and manage your models. You can interact with the Azure Machine Learning workspace through the Studio, Python SDK, and Azure CLI. 

### Create the workspace 

To create the Azure Machine Learning workspace and a compute instance, you'll use the Azure CLI. All necessary commands are grouped in a Shell script for you to execute.

1. In a browser, open the Azure portal at [portal.azure.com](https://portal.azure.com/?azure-portal=true), signing in with your Microsoft account.
2. Select the \[>_] (*Cloud Shell*) button at the top of the page to the right of the search box.The first time you open the cloud shell, you will be asked to choose the type of shell you want to use (*Bash* or *PowerShell*). Select **Bash**.
3. Click on the " Show advanced settings" option in the pop up that opened in the bottom of the screen.  
4. In the Advanced settings page, give  
  - **Resource Group**: Select you existing resource group
  - **Storage account**: Create a new storage account by entering an unique name (should be in small letters)
  - **File share**: type **default** 
  - Create the storage account. Wait for the storage to be created.
5. This opens a Cloud Shell pane at the bottom of the portal. You need to Select **Bash** if not already done.  
6. In the terminal, enter the following commands. You need to replace <...> in the first two lines with your **resource group name** & **an unique name for AML workspace 

    ```bash
    resourceGroupName=<Enter your resource group name here>
    amlWorkspaceName=<Enter name for aml workspace>

    az ml workspace create --name $amlWorkspaceName -g $resourceGroupName

    guid=$(cat /proc/sys/kernel/random/uuid)
    suffix=${guid//[-]/}
    suffix=${suffix:0:18}

    ComputeName="ci${suffix}"

    az ml compute create --name ${ComputeName} --size STANDARD_DS11_V2 --type ComputeInstance -w $amlWorkspaceName -g $resourceGroupName
 
    ```

Wait for the script to complete - this typically takes around 5-10 minutes. 
