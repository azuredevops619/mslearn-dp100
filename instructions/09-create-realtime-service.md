---
lab:
    title: 'Create a real-time inference service'
---
# Create a Real-time Inference Service

There's no point in training and registering machine learning models if you don't plan to make them available for applications to use. In this exercise, you'll deploy a model as a web service for real-time inferencing.

## Before you start

Create aml workspace [here](https://github.com/azuredevops619/mslearn-dp100/blob/main/aml-setup.md) 

## Clone the lab materials

You can use the **Notebooks** page in Azure Machine Learning studio to run notebooks. 

1. In [Azure Machine Learning studio](https://ml.azure.com), view the **Compute** page for your workspace; and on the **Compute Instances** tab, start your compute instance if it is not already running.
1. Select **Terminal** under **Applications** to open a terminal, and ensure that its **Compute** is set to your compute instance and that the current path is the **/users/your-user-name** folder.
1. Enter the following command to clone a Git repository containing notebooks, data, and other files to your workspace:

    ```bash
    git clone https://github.com/azuredevops619/mslearn-dp100.git mslearn-dp100
    ```
1. When the command has completed, in the **Notebooks** pane, click **&#8635;** to refresh the view and verify that a new **/users/*your-user-name*/mslearn-dp100** folder has been created. This folder contains multiple **.ipynb** notebook files.

> **Tip**: New to Python? Use the [Python cheat sheet](cheat-sheets/dp100-cheat-sheet-python.pdf) to understand the code.

## Create a real-time inferencing service

In this exercise, the code to deploy a model as a real-time inferencing service is provided in a notebook.

1. In the **Notebooks** page, browse to the **/users/*your-user-name*/mslearn-dp100** folder where you cloned the notebook repository, and open the **Create a Real-time Inferencing Service** notebook.
2. Then read the notes in the notebook, running each code cell in turn.

## Delete Azure resources

When you finish exploring Azure Machine Learning, you should delete the resources you've created to avoid unnecessary Azure costs.

1. Close the Azure Machine Learning Studio tab and return to the Azure portal.
1. In the Azure portal, on the **Home** page, select **Resource groups**.
1. Click on your resource group name.
1. Select all resources inside the resource group, and select **Delete**. Follow the instructions to delete all resources. Note: Do **not** delete your resource group.  
