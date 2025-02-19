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

### Create Deployments
- kubectl apply -f deployment.yaml
- kubectl get deployments --namespace=default

### Miscellaneous Commands
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
- kubectl delete pods avacado-pod

### Apply label, label-selector and annotation to pods
- kubectl run nginx-prod --image=nginx --namespace=default --labels="ver=1,app=nginx-app,env=prod"
- kubectl run nginx-dev --image=nginx --namespace=default --labels="ver=2,app=nginx-app,env=dev"
- kubectl get pods --show-labels
- kubectl label pods nginx-dev "canary=true"
- kubectl get pods -L canary
- kubectl label pods nginx-dev "canary-"
- kubectl label pods nginx-dev "env=dev" --overwrite=true 

- kubectl get pods --show-labels
- kubectl get pods --selector="ver=2"
- kubectl get pods --selector="app=nginx-app,ver=2"
- kubectl get pods --selector="env in (dev,prod)"
- kubectl label pods nginx-dev "canary=true"
- kubectl get pods --selector="canary"
- kubectl get pods --selector='!canary'
- kubectl get pods -l 'ver=1,!canary' 

- kubectl delete pods --all
- kubectl delete pods --selector="ver=2"
- kubectl delete pods --selector="app=nginx-app,ver=2"
- kubectl delete pods --selector="env in (dev,prod)"
- kubectl delete pods --selector="canary"
- kubectl delete pods --selector='!canary'- 

### Create Services


### Create Deployments
- kubectl delete deployments --all
- kubectl delete deployments --selector="ver=2"
- kubectl delete deployments --selector="app=nginx-app,ver=2"
- kubectl delete deployments --selector="env in (dev,prod)" 
- kubectl delete deployments --selector="canary"
- kubectl delete deployments --selector='!canary'

## selector conversions in yaml
- kubectl get pods --selector="app=nginx-app,env in (dev,prod)"
selector:
  matchLabels:
    app: nginx-app
  matchExpressions:
    - {key: env, operator: In, values: [dev,prod]}

- kubectl get pods --selector="app=nginx-app,ver=2"
selector:
   app: nginx-app
   ver: 2

### selector operators
- "=" and "!=" operators (equality-based)
- "in" and "notin" operators (set-based)









