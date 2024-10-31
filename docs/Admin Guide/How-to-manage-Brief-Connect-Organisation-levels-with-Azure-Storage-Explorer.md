This guide explains how to configure Organisations in Brief Connect using the Azure Storage Explorer application. Follow these steps to set up Organisations level 1-4.

## Before you begin, ensure you have:
*   Write access to the Storage Account in Azure where Brief Connect is deployed
*   Azure Storage Explorer installed on your device

### 1. Open Azure Storage Explorer[](https://dev.azure.com/engagesq/Brief%20Connect/_wiki/wikis/Admin%20Guide/1432/How-to-manage-Brief-Connect-permissions-with-Azure-Storage-Explorer?anchor=1.-open-azure-storage-explorer)

Launch Azure Storage Explorer on your device.

### 2. Connect to Your Storage Account
1.  In Azure Storage Explorer, click on the "Connect" button (plug icon) in the left sidebar
2.  Select "Storage account or service"
3.  Choose one of the following connection methods:
    *   **Connection string**: Select "Connection string (key or SAS)" and paste your storage account connection string
    *   **Azure login**: Select "Azure" and sign in with your Azure credentials
4.  Click "Next"
5.  Click "Connect"

### 3. Navigate to Tables[](https://dev.azure.com/engagesq/Brief%20Connect/_wiki/wikis/Admin%20Guide/1432/How-to-manage-Brief-Connect-permissions-with-Azure-Storage-Explorer?anchor=3.-navigate-to-tables)

1.  In the left navigation pane of Azure Storage Explorer, find and expand your storage account.
2.  Click on **Tables** to display all available tables.

![image.png](.attachments/image-c0aa086e-072d-4e4a-ac92-00d880c3cc6d.png)

3. Select the **organization** table to open it.

![image.png](.attachments/image-5d6b49b0-2d1f-4fbf-b1ee-ad2b5168f7fd.png)

## Setting up the Organisation Structure

In the **organization** table, you will define your organisation’s structure. This structure can include up to four cascading levels.

#### Define the Root Level

1.  To begin, define the Root level, which will appear in the “Organisation Level 1” dropdown in Brief Connect.
    
2.  Click **+Add** at the top of the screen.

![image.png](.attachments/image-8fc821a1-e701-4fd6-b63a-4f8fee437cd3.png)

3. A pop-up will appear:

![image.png](.attachments/image-67426a28-88a2-46d3-8c42-40e34c799b0c.png)

In the pop-up:
*   Set the **PartitionKey** to “Root”.
*   Enter a unique **RowKey** (GUID).
*   Specify the **Name** you want displayed in Brief Connect (e.g., “Head Office”).
Example:

![image.png](.attachments/image-2daa8075-62a0-41ef-a435-d9274dc3fbc7.png)

#### Define the Second Level

1.  Once the Root level is set, you can proceed to create the second level, which will appear in the “Organisation Level 2” dropdown.

For each entry:
*   Set the **PartitionKey** to the **RowKey** of the Organisation Level 1 entry created in the previous step.

Example:

![image.png](.attachments/image-afc4136a-e8e9-4f12-8ad5-efe23cfc374e.png)

_Note that PartitionKey in this screenshot is the same as RowKey in the previous screenshot._

#### Define Levels 3 and 4

Repeat this process for each subsequent level. For each new level, set the **PartitionKey** to the **RowKey** of the previous level’s entry.
