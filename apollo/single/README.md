### Precondition

1. checkout [apollo-build-scripts](https://github.com/nobodyiam/apollo-build-scripts).
2. modify demo.sh to using system environment variables instead.
  ```
  # apollo config db info
  apollo_config_db_url=$APOLLO_CONFIG_DB_URL
  apollo_config_db_username=$APOLLO_CONFIG_DB_USERNAME
  apollo_config_db_password=$APOLLO_CONFIG_DB_PASSWORD

  # apollo portal db info
  apollo_portal_db_url=$APOLLO_PORTAL_DB_URL
  apollo_portal_db_username=$APOLLO_PORTAL_DB_USERNAME
  apollo_portal_db_password=$APOLLO_PORTAL_DB_PASSWORD
  ```
3. docker build -t apollo-standalone:v1.0.0 .  

### Create a apollo single instance

1. kubectl create -n <namespace> -f service.yml
2. kubectl create -n <namespace> -f deployment.yml

For minikube experiment, create a ingress

1. kubectl create -n <namespace> -f ingress.yml
