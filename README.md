# module-10
Container Orchestration with Kubernetes


Main kubectl commands

1. installed minikube and kubectl locally
2. created deployment for nginx
3. edited deployment and set image to specific version
4. created mongo-db deployment
5. deleted deployments afterwards
6. created ngnix-deployment.yml and applied it

--------------------------------------------------

yml config file
1. created ngnix-service.yml and applied it
2. checked service for ips and pods with -o wide to see their ips

--------------------------------------------------

Deploying app in kubernetes cluster
1. copied yml files from gitlab
2. added port and env to mongo.yml
3. added username/password in base64 in mongo-secret.yml
4. applied secret
5. added secretKeyRef in mongo.yml
6. added service in mongo.yml, appkied afterwards
7. added DB_URL to mongo-configmap.yml
8. added configMapKeyRef to mongo-express.yml and applied it.
9. Pod was in state crashloop, corrected typo in mongo-express.yml and applied again
10. added service in mongo-express.yml and applied 

--------------------------------------------------

Namespaces
1. created namespace manually and set it as default
2. installed kubens in wsl

--------------------------------------------------

Ingress
1. copied dashboard-ingress.yml file from gitlab
2. enabled ingress addon for minikube
3. tested minikube dashboard
4. applied dashboard-ingress.yml
5. edited hosts file
6. ran minikube tunnel

--------------------------------------------------

Volumes
1. 



--------------------------------------------------

Reference: DevOps Bootcamp and TWN