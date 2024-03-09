# Minikube

> minikube quickly sets up a local Kubernetes cluster

## Install Minikube

```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-arm64
sudo install minikube-darwin-arm64 /usr/local/bin/minikube
```

## Start Cluster

```bash
minikube start --driver qemu --network builtin
```

## Interact with Cluster

```bash
% minikube kubectl -- get pods -A
NAMESPACE     NAME                               READY   STATUS    RESTARTS        AGE
kube-system   coredns-5dd5756b68-wcnh9           1/1     Running   1 (7m20s ago)   8m49s
kube-system   etcd-minikube                      1/1     Running   2 (2m39s ago)   9m2s
kube-system   kube-apiserver-minikube            1/1     Running   2 (2m29s ago)   9m2s
kube-system   kube-controller-manager-minikube   1/1     Running   2 (2m39s ago)   9m2s
kube-system   kube-proxy-mvtcq                   1/1     Running   2 (2m39s ago)   8m50s
kube-system   kube-scheduler-minikube            1/1     Running   2 (2m39s ago)   9m2s
kube-system   storage-provisioner                1/1     Running   4 (16s ago)     9m1s
```
> [!NOTE]
> What are they?
> * `coredns` is a flexible, extensible DNS server that can serve as the Kubernetes cluster DNS
> * `etcd` is a consistent and highly-available key value store used as Kubernetes' backing store for all cluster data
> * `kube-apiserver` validates and configures data for the api objects which include pods, services, replicationcontrollers, and others
> * `kube-controller-manager` is a daemon that embeds the core control loops shipped with Kubernetes
> * `kube-proxy` runs on each node
> * `kube-scheduler` is a control plane process which assigns Pods to Nodes
> * `storage-provisioner` provides pods with persistent storage
