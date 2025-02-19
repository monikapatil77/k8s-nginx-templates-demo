## Create pod from manifest file
### Create Pod
- kubectl apply -f pod.yaml
- kubectl get pods
- kubectl get pods --namespace=default 
- kubectl logs demo
- kubectl delete -f pod.yaml 
- kubectl describe pods demo

### Create Services
- kubectl get services --namespace=default
-

### Create Deployments
- kubectl apply -f deployment.yaml
- kubectl get deployments --namespace=default
- 

###
- kubectl get componentstatuses
- kubectl cluster-info
- kubectl config get-contexts
- kubectl get namespaces
- kubectl -- get pods -A
- kubectl get daemonSets --namespace=kube-system

## Create pod from command line
### Create Pod
- kubectl run avacado-pod --image=avacado-web
- kubectl run nginx --image=nginx --restart=Never

### Create Services


### Create Deployments








