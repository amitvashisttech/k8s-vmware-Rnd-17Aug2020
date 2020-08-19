# Kubernetes Dashboard Setup

Step 1: "Deploy K8s Dashboard" 
```
kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.0.0-rc7/aio/deploy/recommended.yaml
```

Step 2: "Create a Sample User for Login"
```
kubectl create -f sample-user.yaml
```

Step:3 "Expose kubernetes-dashboard Service on NodePort, then try to access the dashbaod https://<node-ip>:<node-port>"
```
kubectl edit svc  kubernetes-dashboard -n kubernetes-dashboard  
```
Note: Replace ClusterIP to NodePort


Step:4 "Retrive the token-id of newly created Admin-1"
```
kubectl get secret -n kubernetes-dashboard
```

Step:5 "Grab the Token & Use the same to login to K8s Dashboard"
```
kubectl describe secret  admin-user-1-token-t7gsn -n kubernetes-dashboard
```
