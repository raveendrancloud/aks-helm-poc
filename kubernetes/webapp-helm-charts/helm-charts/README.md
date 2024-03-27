# Helm apply order

1. MYSQL CHART & INGRESS CONTROLLER CHART SHOULD BE APPLIED FIRST!
2. SET DB PASSWORD IN SHOPAPI CHART values file. Use command 'kubectl get secret --namespace default mysql -o jsonpath="{.data.mysql-root-password}"' to retrive it.

3. helm install website ./website-chart --wait  
4. helm install shopapi ./shopapi-chart --wait  
5. helm install shopui ./shopui-chart --wait  


### shopapi-chart
    > shopapi + ingress for entire webapp

### shopui-chart
    > shopui

### website-chart
    > website