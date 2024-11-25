#HPA Horizontal pod scaling
the two main conditions  to for the HPA
we need to install the  metrics in the server

```
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/high-availability-1.21+.yaml
```

should mention the resource section in the pod 
example:

```
spec:
      containers:
      - name: frontend
        image: joindevops/frontend:v1
        resources:
          requests:
            cpu: 100m
            memory: 128Mi
          limits:
            cpu: 100m
            memory: 128Mi
```




command to to check the utilistion of the pods 

```
kubectl top pods
```

Command to check  the avarage status of pod

```
kubectl get hpa
```
