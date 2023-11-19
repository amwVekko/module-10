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

ConfigMap & Secret Volume
1. copied starting code from gitlab
2. applied config and secret file
3. configured config and secret volumes/mounts in mosquitto.yml
4. applied mosquitto.yml
5. execed into the container and checked secret and config file

--------------------------------------------------

Helm Demo - Managed K8s cluster
1. created Linode account
2. created K8s cluster with 2 nodes
3. copied helm yml files from gitlab
4. copied test-kubeconfig.yaml file from linode and set access to 400
5. export = KUBECONFIG=test-kubeconfig.yaml
6. installed Helm in WSL with apt using https://helm.sh/docs/intro/install/
7. added helm repo bitnami
8. installed mongodb with values file helm-mongodb.yml
9. checked in linode for PVCs
10. applied helm-mongo-express.yml
11. added helm repo ingress-nginx
12. helm install nginx-ingress ingress-nginx/ingress-nginx --set controller.publishService.enabled=true
13. For Hostname i used no-ip.com to test with amwgaming.ddns.net
14. applied helm-ingress.yml
15. added some data in mongodb, scaled pods down to 0 with kubectl scale
16. scaled up to 3 and checked data is still available in mongodb

--------------------------------------------------

Deploying Images in Kubernetes from private Docker repository
1. logged into AWS provided docker login command
2. logged into AWS from inside minikube with AWS token
3. copied config.json file from inside minikube to WSL
4. encrypted token and added to secrets file
5. created secret with kubectl create secret generic my-registry-key
6. added image name with repo and tag to my-app-deplyoment.yml
7. added PullPolicy to pull image always and imagePullSecret
8. applied my-app-deplyoment.yml
9. removed base64 encrypted token from docker-secret.yml to be safe

--------------------------------------------------

Deploy microservice application
1. cloned gitlab project "microservice-demo" and config.yml
2. created new k8s cluster on linode with 3 worker nodes
3. downloaded kubeconfig.yml, set access to 400 and export = KUBECONFIG
4. created namespace and applied config.yml to it
5. tested access to shop via browser

--------------------------------------------------

Reference: DevOps Bootcamp and TWN