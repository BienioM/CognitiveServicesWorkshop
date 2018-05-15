# Deploy the custom vision service container to Azure Container Instance

## Create a resource group
```
az group create --name <resource group> --location <location>
```

## Create a container
```
az container create --resource-group <resource group> --name <container name> --image microsoft/aci-helloworld --dns-name-label aci-demo --ports 80
```

## Show the container's status
```
az container show --resource-group <Your resource group> --name <Container name> --name <Container name> --query "{FQDN:ipAddress.fqdn,ProvisioningState:provisioningState}" --out table
```
