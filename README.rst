OSP DCI Ansible Hooks
=====================

INTRO
-----

Playbooks to deploy and configure RHOSP11 undercloud/overcloud on a pre-defined hw setup

Refer to https://github.com/redhat-cip/dci-ansible-agent for hooks to be implemented

------------

TASK
----

* Undercloud installation - undercloud.yml
* Overcloud installation - overcloud.yml
* Post configuration on controller node for network, instance image and cinder backends - post-config.yml
* Teardown the environment by deleting the undercloud director VM - teardown.yml

How to Use
----

* Install ansible machine, extra pyvmomi package is required for vmware module
* Edit ansible.cfg file
    * host_key_checking = false
    * inventory = /root/osp_hooks/hosts
* Download this tool, and modify varilables with your own hw setup
    * hosts file (only director IP, leave overcloud section untouched)
    * var/main.yml
    * settings.ini
    * files/cinder_backends (modify x.x.x.x, xxxx for real ip and password) 
