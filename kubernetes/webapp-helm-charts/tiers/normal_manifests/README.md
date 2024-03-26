# Mysql helm chart

helm repo add bitnami https://charts.bitnami.com/bitnami
helm install mysql bitnami/mysql --version 10.1.0 --set auth.database=bookstore

kubectl get secret --namespace default mysql -o jsonpath="{.data.mysql-root-password}"      
	> place it on secret.yaml data.DB_PASSWORD

# Nginx ingress controller helm chart

helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
helm install my-ingress-nginx ingress-nginx/ingress-nginx --version 4.10.0