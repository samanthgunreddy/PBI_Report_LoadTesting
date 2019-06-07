# Power BI Dedicated Capacity Load Assessment

This package includes:  
- **Powershell script** (starting point) - Interactively gets inputs from the user and updates the PBIToken and PBIReport files.
- **PBIToken** (JS Object File) file which stores Aad access token for the connections to work.
- **PBIReport** (JS Object File) file which stores report parameters including report url, filter parameters.
- **HTML + Javascript single pager** - Uses PBIToken and PBIReport files to get access token, report details and initiates the load.

### Description:
- This package helps in conducting load test from client side without a need for web instance or App registration. Powershell script utilizes PowerBI modules to get Aad access token and to retrieve workspace, reports etc. for the authenticated user.
- Powershell script is desgined as an interactive UI to get inputs from user and configure multiple reports.
- Script provides an option to enter the number of instances/sessions to be run for each report.

##### Notes:
- By default, Aad access token expires in 60 minutes. Reports will run for 60 minutes once initiated and stop with error once access token expires.

###### HTML report file has been designed and implemented by [Sergei Gundorov](https://github.com/sergeig888).
