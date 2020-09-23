# OCP4-pre-reqs
Playbook to deploy Image Registry, DNS, Web Server and HAProxy to meet the requirements of an OCP deployment. Everything will be installed and accessed via a single helper node. This could be used for simulating a clients already established environment before you a consulting engagement to deploy OCP4.

Setup a Image Registry
Setup an Apache Webserver
Setup DNS
Setup HAProxy

## Pre-reqs

- Ansible 2.9> (Not tested on <2.9)
- python >= 2.7 with pip package

The below Python and Package dependencies are installed in the pre-flight role (They are shown here for reference only)
### Python modules
- netaddr
- passlib

### Packages
- python3-policycoreutils

### OS
- RHEL8 / CENTOS8 (Not yet tested on 7)


## Deployment instructions
Complete the vars.yml file to match your network and node details. 

Note: This is only designed to be run agaist localhost at the minute but will be refactored to take an inventory.

Run the following to playbook

```bash
ansible-playbook ocp_pre-reqs.yml -e @vars.yml
```