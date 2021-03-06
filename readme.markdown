AzureBlobDrive
==============
AzureBlobDrive allows you to mount Azure Blob Storage as a drive in Windows. This is useful if your Azure application needs to write files, or you want to easily access Blob Storage from your desktop computer.

AzureBlobDrive is based on the Dokan user mode file system for Windows: http://dokan-dev.net/en/

Watch a video AzureBlobDrive: http://screencast.com/t/thtRbQvZq1Pr

Download the console application here: https://github.com/downloads/richorama/AzureBlobDrive/Two10.AzureBlobDrive.Console.zip
(you will need to update the config file to set your storage account details)

Installation
------------

AzureBlobDrive requires the Dokan library to be installed, this can be downloaded from here: http://dokan-dev.net/en/download/#dokan

If you run Two10.AzureBlobDrive.exe, a new drive will appear in My Computer, which lists the containers in your storage account.

Configuration
-------------

By default, AzureBlobDrive mounts Blob Storage on the R:\ drive, however you can change this in the .config file, by changing the 'DriveLetter' setting.

AzureBlobDrive will also default to the Storage Emulator. Modify the 'AzureConnectionString' setting to point it towards your Azure Storage (i.e. DefaultEndpointsProtocol=https;AccountName=YOUR_ACCOUNT_NAME;AccountKey=YOUR_ACCOUNT_KEY )

Limitations
-----------

 - Root folder names (containers) must be in lower case, and cannot contain spaces and other special characters.
 - Performance is poor, and large files are not recommended.
 - Files and folders are cached for one minute, so changes made by other machines may not be instantly viewable.
 - Files (blobs) cannot be empty (i.e. have a zero size).

About
-----
AzureBlobDrive was written by Richard Astbury. For more information, or Azure consultancy, please contact two10 degrees: http://www.two10degrees.com/ 


