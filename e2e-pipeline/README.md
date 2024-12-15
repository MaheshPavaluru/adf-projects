# adf-simpleProject
this is a repo with simple azure data factory project.


Project Overview

The solution is designed to automatically trigger a pipeline in response to new file uploads or modifications in a specified Azure Storage container. It supports end-to-end data ingestion and transformation, making it suitable for real-time and batch processing scenarios.

Features

Event-Driven Trigger: Automatically starts the pipeline when a new blob is created or modified in the storage container.

Data Transformations: Executes transformations including data cleansing, enrichment, and aggregation.

Scalable Workflow: Designed to handle large volumes of data.

Error Handling: Includes mechanisms for logging and retrying failed activities.

Architecture

Trigger: Event-based trigger configured on an Azure Blob Storage account.

Pipeline: ADF pipeline orchestrates data processing:

Source: Reads data from the Azure Blob Storage container.

Transformations: Executes transformations using Data Flows or custom logic in Azure Databricks/SQL.

Sink: Writes the processed data to an Azure Data Lake or SQL Database.

Monitoring: Tracks pipeline execution via ADF Monitoring tools.

Getting Started

Prerequisites

Ensure the following resources are available:

Azure Subscription: Active Azure subscription to deploy ADF and associated resources.

Azure Resources:

Azure Data Factory instance

Azure Blob Storage account

Azure Data Lake or SQL Database for storing processed data

Azure CLI: Installed for deployment (optional).

Deployment

Clone the Repository:

git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name

Import ADF Artifacts:

Open Azure Data Factory Studio.

Navigate to Manage > ARM Template > Import ARM Template.

Upload the arm_template.json file from this repository.

Configure Linked Services:

Update connection strings for Azure Blob Storage, Azure Data Lake, and any other data stores in the ADF linked services section.

Set Up Event Grid Trigger:

Go to Azure Portal > Event Grid.

Create a subscription to your Blob Storage account.

Link the subscription to the ADF pipeline.

Publish and Test:

Publish the ADF pipeline.

Upload a file to the configured Azure Blob Storage container to trigger the pipeline.

Usage

Upload Files: Place your data files in the designated Azure Blob Storage container.

Pipeline Execution: The pipeline will automatically start, perform transformations, and load the data into the target destination.

Monitor Runs: Use the Monitor tab in ADF Studio to track the status of pipeline runs, view logs, and debug issues.
