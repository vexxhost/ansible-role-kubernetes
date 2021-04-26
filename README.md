# ansible-role-kubernetes
Ansible role to deploy highly available Kubernetes clusters using `kubeadm`.

## Usage
You'll need to define the following variables and the playbook will take care
of the rest:

```
# name of the Ansible group containing all controllers
kubernetes_control_plane_group: controllers

# Hostname (which should resolve to the VIP below)
kubernetes_hostname: kubernetes.public.ams1.vexxhost.net

# Virtual IP address to be hosted across all systems
kubernetes_keepalived_vip: 10.121.1.200

# VRRP ID
kubernetes_keepalived_vrid: 10
```