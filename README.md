# Kubernetes-Network-Policy
### To Implement the Network Polciy in Kubernetes Enviornmetns you can implement the one the following network solution 
Install a Network Policy Provider https://kubernetes.io/docs/tasks/administer-cluster/network-policy-provider/
- Kube-router
- Calico
- Romana
- Wave-net

Install a Wave-net Network Policy https://github.com/weaveworks/weave/blob/master/site/kubernetes/kube-addon.md#network-policy

- Weave Net can be installed onto your CNI-enabled Kubernetes cluster with a single command:
```bash
kubectl apply -f https://github.com/weaveworks/weave/releases/download/v2.8.1/weave-daemonset-k8s.yaml    
```
- Test the installation
```bash
kubectl get pods -n kube-system -o wide    
```
-The output is similar to this:

```bash
NAME                                    READY     STATUS    RESTARTS   AGE       IP              NODE
weave-net-1t1qg                         2/2       Running   0          9d        192.168.2.10    worknode3
weave-net-231d7                         2/2       Running   1          7d        10.2.0.17       worknodegpu
weave-net-7nmwt                         2/2       Running   3          9d        192.168.2.131   masternode
weave-net-pmw8w                         2/2       Running   0          9d        192.168.2.216   worknode2    
```
