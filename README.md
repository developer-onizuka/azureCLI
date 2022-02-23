# azureCLI


# 1. Pull Ubuntu and run
```
$ docker run --rm -it --name ubuntu ubuntu:18.04 /bin/bash
```

# 2. Install PowerShell
https://docs.microsoft.com/en-us/learn/modules/control-azure-services-with-cli/3-exercise-install-and-run-the-azure-cli?pivots=linux
```
# apt-get update
# apt-get install -y curl sudo
# apt-get install -y gnupg gnupg2 gnupg1
# apt-get install -y lsb-release
# AZ_REPO=$(lsb_release -cs)
# echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ $AZ_REPO main" | \
  sudo tee /etc/apt/sources.list.d/azure-cli.list
# curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
# sudo apt-get install apt-transport-https
# sudo apt-get update && sudo apt-get install azure-cli
```

# 3. Check version of azCLI
```
# az --version
azure-cli                         2.33.1

core                              2.33.1
telemetry                          1.0.6

Dependencies:
msal                              1.16.0
azure-mgmt-resource               20.0.0

Python location '/opt/az/bin/python3'
Extensions directory '/root/.azure/cliextensions'

Python (Linux) 3.6.10 (default, Feb 14 2022, 04:03:52) 
[GCC 7.5.0]

Legal docs and information: aka.ms/AzureCliLegal


Your CLI is up-to-date.

Please let us know how we are doing: https://aka.ms/azureclihats
and let us know if you're interested in trying out our newest features: https://aka.ms/CLIUXstudy
```


# 4. How do you find the particular commands you need (az find)
```
# az find cosmosdb
Finding examples...

Here are the most common ways to use [cosmosdb]: 

Get the details of an Azure Cosmos DB database account. (autogenerated)
az cosmosdb show --name MyCosmosDBDatabaseAccount --resource-group MyResourceGroup

Update an Azure Cosmos DB database account. (autogenerated)
az cosmosdb update --ip-range-filter {ip-range-filter} --name MyCosmosDBDatabaseAccount --resource-group MyResourceGroup

Deletes an Azure Cosmos DB database account. (autogenerated)
az cosmosdb delete --name MyCosmosDBDatabaseAccount --resource-group MyResourceGroup

Please let us know how we are doing: https://aka.ms/azureclihats
```
```
# az find "az vm"  
Finding examples...

Here are the most common ways to use [az vm]: 

List all VMs.
az vm list

Place the CLI in a waiting state until a condition of the VM is met. (autogenerated)
az vm wait --custom {custom} --name MyVm --resource-group MyResourceGroup

Start a stopped VM. (autogenerated)
az vm start --name MyVm --resource-group MyResourceGroup

Please let us know how we are doing: https://aka.ms/azureclihats
```
