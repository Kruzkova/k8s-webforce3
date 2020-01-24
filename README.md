# k8s-webforce3

## Check
```shell script
  kubectl get nodes
  kubectl get node
  kubectl get node -o wide:

## Deployment example
  kubectl create deployment nginx --image=nginx
  kubectl get deployments
  kubectl describe deployment nginx
  kubectl get events
  kubectl get deployment nginx -o yaml 
  kubectl get deployment nginx -o yaml > first.yaml
  kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep admin-user | awk '{print $1}' )
```

## cpu limits 
```
k create deployment 

k replace -f xx.yaml or json

```
## Namespace
```
k create namespace low-usage-limit
k get namespace 
k --namespace=low-usage-limit create -f low-ressource-range.yaml

k get limitrange -A

k -n low-usage-limit get pod limited-hog-hexacode64 -o yaml "> export.yaml"
k create -f file.yaml
k delete pod -l system=IsolatedPod
```
## demonset 

```
k create -f ds
k get pod -o wide
```