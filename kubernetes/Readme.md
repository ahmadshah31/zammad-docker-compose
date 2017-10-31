# Zammad kubernetes example deployment

## Perquisites

- On every node you need to set `sysctl -w vm.max_map_count=262144`
- Change the ingress to your needs.


## Deploy zammad

### Install on Minikube example

* Install kubectl
  * https://kubernetes.io/docs/tasks/tools/install-kubectl/
* Install Minkube
  * https://github.com/kubernetes/minikube
* minikube start --memory=4096 --cpus=2
* minikube ssh
  * su -
  * sysctl -w vm.max_map_count=262144
* kubectl apply -f .
* minikube dashboard
  * switch to namespace "zammad"
  * open "Overview" and wait until all pods are green