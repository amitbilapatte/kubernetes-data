# kubernetes-data
managing data with kubernetes volumes

- **Kubernetes Volume Types**
- `emptyDir` : In this volume type, a empty directory is created on start of container, and data is stored,  but it can't survive the container crash
- `hostPath` : In this volume type, if we have multiple replicas of a container the data is stored just like *bind mounts* by providing/creating a directory on host machine. even if one pod crashes other replica pod can provide the service. but this is limited to single node only.
- `CSI` (Container Storage Interface):
- `nfs` (Network File System server):
- and there are many other volume types in kubenetes.
