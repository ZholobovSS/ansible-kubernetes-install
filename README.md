Ansible role: zh2s.kubernetes_install
=========

Install kubernetes with `Ingress-nginx` and `MetalLB` as a network load-balancer implementation

Requirements
------------

Ubuntu 22.04 or higher
One or more VDS for master node (min 2 CPU, min 4GB RAM) on each machine
One or more VDS for worker node (min 4 CPU, min 4GB RAM) on each machine

Role Variables
--------------

    kubernetes:
      metallb_version:
    
    user_name:

Dependencies
------------

Before start this role you should create non-root user. Name of this user you should set in `user_name` variable

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      vars:
        kubernetes:
          metallb_version: "0.13.7"
        user_name: devops
      roles:
         - { role: zh2s.kubernetes_install }

