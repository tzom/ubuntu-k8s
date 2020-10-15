# ubuntu-k8s

Deploys ubuntu pods on kubernetes including a persistent storage.
This is useful to have a **shell** that also has **access to persistent storage** in kubernetes.

### deploy ubuntu pods and a ask for a persistent nfs storage volume (persistent-volume-claim - short pvc):

> kubectl apply -f unbuntu.yaml -n ``<namespace>``

### check pods availability:

> kubectl get pods -n ``<namespace>``

### get the shell of a running ubuntu pod (i.e. use a specific pod-name): 

> kubectl exec -n ``<namespace>`` -it ``<pod-name>`` -- /bin/bash

should give you this:
```
root@ubuntu-deployment-7dbff66d58-tbqr5:/# 
root@ubuntu-deployment-7dbff66d58-tbqr5:/# cd /mnt/nfs
root@ubuntu-deployment-7dbff66d58-tbqr5:/mnt/nfs# 
```
Have fun!