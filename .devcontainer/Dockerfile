# Find the Dockerfile for mcr.microsoft.com/azure-functions/powershell:3.0-powershell${VARIANT}-core-tools at this URL
# https://github.com/Azure/azure-functions-docker/blob/master/host/3.0/buster/amd64/powershell

# Update the VARIANT arg in devcontainer.json to pick a supported PowerShell version: 7, 6
ARG VARIANT=7
FROM mcr.microsoft.com/azure-functions/powershell:3.0-powershell${VARIANT}-core-tools
RUN echo "\{\r\n\
  \"IsEncrypted\": false,\r\n\
  \"Values\": {\r\n\
    \"AzureWebJobsStorage\": \"UseDevelopmentStorage=true\",\r\n\
    \"FUNCTIONS_WORKER_RUNTIME\": \"powershell\"\r\n\
  }\r\n\
}" > /home/vscode/workspace/dataverse-ad-user-sync-powershell-azure-functions/local.settings.json
