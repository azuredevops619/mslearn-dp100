---
lab:
    title: 'Run experiments'
---
# Run Experiments

Experiments are at the core of a data scientist's work. In Azure Machine Learning, an *experiment* is used to run a script or a pipeline, and usually generates outputs and records metrics. In this exercise, you will use the Azure Machine Learning SDK to run Python code as experiments.

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

## Verify the Azure Machine Learning SDK is installed

The Azure Machine Learning SDK is installed by default on your compute instance. Follow these steps to verify the installation.

1. In the **Notebooks** page, create a new **Terminal** if it's not open anymore. This will open a new tab with a command shell.
2. Enter the following command to install the Azure ML SDK:

    ```bash
    pip install azureml-sdk
    ```

    Note the version of the SDK package installed.

3. The **azureml-sdk** SDK package provides the most important libraries needed to work with Azure Machine Learning> However, there are some additional packages that contain other useful libraries not included in the main SDK package. Use the following command to install the **azureml-widgets** package, which contains libraries for displaying Azure Machine Learning information in notebooks:

    ```bash
    pip install azureml-widgets
    ```

4. Close the **Terminal** tab.

> **More Information**: For more details about installing the Azure ML SDK and its optional components, see the [Azure ML SDK Documentation](https://docs.microsoft.com/python/api/overview/azure/ml/install?view=azure-ml-py).

## Run experiments in a notebook

Experiments in Azure Machine Learning need to be initiated from some sort of *control* layer; often a script or program. In this exercise, you'll use a notebook to control experiments.

1. In the **Notebooks** page, browse to the **/users/*your-user-name*/mslearn-dp100** folder where you cloned the notebook repository, and open the **Run Experiments** notebook.
2. Then read the notes in the notebook, running each code cell in turn.

## Delete Azure resources

When you finish exploring Azure Machine Learning, you should delete the resources you've created to avoid unnecessary Azure costs.

1. Close the Azure Machine Learning Studio tab and return to the Azure portal.
1. In the Azure portal, on the **Home** page, select **Resource groups**.
1. Click on your resource group name.
1. Select all resources inside the resource group, and select **Delete**. Follow the instructions to delete all resources. Note: Do **not** delete your resource group.  
