# Deploy the custom vision service container to Azure Container Instance

## Create a resource group
```
az group create --name <Your resource group> --location <Location>
```

## Create a container
```
az container create --resource-group <Your resource group> --name <Container name> --image microsoft/aci-helloworld --dns-name aci-demo --ports 80
```

## Show the container's status
```
az container show --resource-group <Your resource group> --name <Container name> --name <Container name> --query "{FQDN:ipAddress.fqdn,ProvisioningState:provisioningState}" --out table
```
