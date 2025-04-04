We can expose an application to the internet which are running on a set of pods in k8s by using some services in K8S
# 1. Cluster IP
# 2. Node port
# 3. Load balancer
Node port range can be 30000 - 32767


<img width="662" alt="NodePort" src="https://github.com/user-attachments/assets/639c333e-b81a-42b8-adb2-04e470494b62" />


# deployment.yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: my-app-deployment
spec:
  replicas: 3  # Number of replicas (pods)
  selector:
    matchLabels:
      app: my-app  # Label selector to match pods
  template:
    metadata:
      labels:
        app: my-app  # Same label as in the selector
    spec:
      containers:
      - name: my-app
        image: my-app-image:latest
        ports:
        - containerPort: 80  # Expose port 80 on each pod
