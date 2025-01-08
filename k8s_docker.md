-Docker: Container platform
-K8s: Container orchistration platform

Drawbacks for Docker
- Single Host ( In k8s it is a cluster so it will have many nodes. So we can over come this single host problem )
- Auto scaling ( In k8s we have HPA )
- Auto healing ( In K8s if the conatiner is getting failed before that it will roll out the new container )
- Enterprise level support ( K8s is open source so we can get many developments required )
To overcome the above issue in docker we can use the K8S

![image](https://github.com/user-attachments/assets/411305ee-4750-47ad-bb15-8ddfea212507)

1. API SERVER: Face of the k8s and take the incoming requests to the K8s.
2. Scheduler: Schedule the pods on the specific node as per the availability
3. Controller: Take care of the replica sets and controls it.
4. etcd: It will have the back up of the cluster data.
5. kubelet: Check whether the pod is up and running or not. If pod is not up then it will inform to API server so that it can ask scheduler to schedule the pod.
6. Kubeproxy: It will handle the networking, ip address and load balancing of the pods.
7. Container run time: It will take care of the container to run as the code ( java, .Net etc ) used in it. In docker we will use docker shrim.
