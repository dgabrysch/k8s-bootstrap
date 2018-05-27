# k8s-bootstrap
Bootstrapping kubernetes clusters

This repo contains the necessary stuff to run a 3 Master / ETCD Cluster running 
on-premise on RHEL and CentOS.

Please note: Running etcd inside a HA-k8s Cluster is fine (got to be timing stuff nicely though) - we are using the Centos ETCD package here, this may or may not be your choice.
Maybe there will be another version of these playbooks with this feature too.

Loadbalancer setup should be done by you yourself, there is a possibility to automate that too using the k8s cluster. If this is a needed feature - please let me know.

The following versions are running with the playbooks:

Etcd:

etcd-3.2.15-1.el7.x86_64

Kubernetes:

kubelet-1.9.4-0.x86_64
kubeadm-1.9.4-0.x86_64
kubernetes-cni-0.6.0-0.x86_64
kubectl-1.9.4-0.x86_64

Calico:

quay.io/calico/node:v3.0.2
quay.io/calico/cni:v2.0.0
quay.io/calico/kube-controllers:v2.0.0

Currently Internet access is necessary, this will be changed in the next versions.

Further project plans:
- All necessary components should run on at least once per master node
- Add some optioning for bootstrapping
- LDAP Auth :)


