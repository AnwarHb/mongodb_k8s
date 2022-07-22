## Kubernetes practise
The aim is to deploy 2 applications: mongoDB, mongoexpress.
I created a mongoDb pod with an internal service and a mongoexpress pod with an external service, the connection between the two pods is achieved by a configmap that contains the DB_url and a secret object that contains the username and password.

#### Objects :
- mongodb deployment 
- mongodb service
- mongodb secret 
- mongoexpress depolyment
- mongoexpress service 
- mongodb configmap

You should install minikube and kubectl installed in your machine to run the code.

### Run locally:
- clone the code repository : `git clonehttps://github.com/AnwarHb/mongodb_k8s.git `
- start minikube `minikube start`
- apply the yaml files: 
 1. `kubectl apply -f mongo_secret.yml`
 2. `kubectl apply -f mango_deployment.yml`
 3. `Kubectl apply -f mongo_configmap.yml`
 4. `Kubectl apply -f mongo_express.yml`
- start the mongoexpress service: `minikube service mongo-express-service`

[![](https://github.com/AnwarHb/mongodb_k8s/blob/main/mongoExpress%20service.png?raw=true)](https://github.com/AnwarHb/mongodb_k8s/blob/main/mongoExpress%20service.png?raw=true)

you can now access the app in your browser :
[![](https://github.com/AnwarHb/mongodb_k8s/blob/main/app_in_browser.png?raw=true)](https://github.com/AnwarHb/mongodb_k8s/blob/main/app_in_browser.png?raw=true)
