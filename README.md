configure_master
=========

Configures master for k8s: kubeadm init and compies join command and instal helm.

Requirements
------------
You have to check defaults and just start this role!

Role Variables
--------------
Defaults:
```
pod_network_cidr: 10.244.0.0/16
cri_socket: /run/containerd/containerd.sock
control_plane_endpoint: k8smaster.example.net
skip_phases: addon/kube-proxy
# for calico: cidr: 192.168.0.0/16
helm_version: 'v3.10.2'
helm_platform: linux
helm_arch: amd64
helm_repo_path: "https://get.helm.sh"
helm_bin_path: /usr/local/bin/helm
```
Example Playbook
----------------
```
- hosts: servers
  roles:
     - role: configure_master
```
Author Information
------------------

nodegopher@gmail.com
Nagornov Vyacheslav
