# chaos-mesh-demo
This repo contains chaos experiments for demo purposes

# Environment
[Minikube](https://kubernetes.io/ru/docs/tasks/tools/install-minikube/)

# Demo application
[GCP microservices-demo](https://github.com/GoogleCloudPlatform/microservices-demo)

# Experiments
## PodChaos
### CartService one replica fault 
*Description:* One of the running pods in the cart service deployment has become unavailable due to a pod fault, but the others remain running. There is no significant impact on the user experience, and functionality should be available for the end user.


### before experiment:
scale up cartservice deployment:
```bash
kubectl scale deployments/cartservice --replicas=2
```

### sceanrio
1. apply chaos experiment
```bash
kubectl apply -f experiments/podchaos/cartservice-one-pod-fault.yaml
```
2. check status of experiment
3. check user scenario (tbd)

### CartService all replicas fault
tbd
