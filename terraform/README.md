terraform init
terraform plan
terraform apply --auto-approve

az aks get-credentials --resource-group aks-helm-poc --name aks --overwrite-existing --admin