# Chicó
Chicó is a collection of automatic webscrapping scripts to help analyse public expenditures from Pernambuco Legislative Assembly (ALEPE).

## Azure Functions
This project is a simple port from local running code to scheduled azure functions. It can be enhanced to consider edge cases such as website unavailability.

Other functions may be added in the future.

- timedCheckIndemnityFunds ("Verbas indenizatórias")

## Develop

Prepare your Azure Functions development environment for Python (https://docs.microsoft.com/pt-br/azure/azure-functions/)

1. Configure Azure Storage to have a container named "data-output"
1. Clone this repository
2. Run in development mode


local.settings.json
<pre>
{
  "IsEncrypted": false,
  "Values": {
    "AzureWebJobsStorage": "ConnectionStringHere",
    "FUNCTIONS_WORKER_RUNTIME": "python"
  }
}
</pre>

### TODO

- Refactor usage of python constants and lists
- Include exception handling notifying configured e-mail addresses in case of failure (and success?)
- Port to azure functions: Law Project Analysis

## Libs
- BeautifulSoup
- Requests
- Pandas
- Azure Functions
- Azure Storage Blob