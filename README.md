# SSRS_Migrate
Migrate SQL Server Reporting Services Objects to New Server

(Because Microsoft cant create a valid upgrade tool between 2016 and 2017)

Requirements: 
* Active Directory Powershell Module (RSAT)
* Powershell 5.1

Powershell scripts to Migrate SSRS Objects from 2008+ Servers to anything newer.

Uses SQL, WMI, SOAP and REST to export the following objects:
* RDL Reports with embedded DataSources/DataSets
* Shared DataSources
* Shared Data Sets
* PowerBi PBIX files
* Mobile Reports
* KPIs
* Shared Schedules
* Subscriptions
* Users
* Folder Tree Structure
* Folder and Report Permissions
* Config Files
* Encryption Key

Companion Import Script will restore these objects in the following order:
* Users
* FolderTree Structure with Permissions/Inheritance
* Shared Schedules
* Shared Data Sources
* Shared DataSets
* RDL Reports with embedded Data Sources/DataSets and Permissions/Inheritance
* Subscriptions

Must be Sysadmin on both SQL servers for this to work

Please send FeedBack to dev at insyncva dot com
