# kubernetes-data
managing data with kubernetes volumes

- **Kubernetes Volume Types**
- `emptyDir` : In this volume type, a empty directory is created on start of container, and data is stored,  but it can't survive the container crash
- `hostPath` : In this volume type, if we have multiple replicas of a container the data is stored just like *bind mounts* by providing/creating a directory on host machine. even if one pod crashes other replica pod can provide the service. but this is limited to single node only.
- `nfs` (Network File System server):
- and there are many other volume types in kubenetes.

- `CSI` (Container Storage Interface):
 In our local environment, we use `minikube` which works with `only one node` so in this case we can handle data with `hostPath`, but in real case scenario, we'll have to work with `multiple nodes` and every other node may have different data, so for storing/presisting this data we will need `CSI`.
- `hostPath` partially works around that in "One-Node" environments
- `Persistent Volumes` can work `Pod and Node-Independent Volumes`
