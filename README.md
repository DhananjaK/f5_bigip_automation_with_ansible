Role Name
=========

In this Ansible role, we will cover the following workflow, 

Validate the node, virtual server and pool existence → Create new nodes →  Create pool   → Add nodes to the created pool → Create virtual server → Attach pool to the virtual server.  


Requirements
------------

You must have an F5-BigIP LTM appliance to test this Ansible role.

Role Variables
--------------

# Pool Information
load_balancing_method: []
pool_name: []

# Member Information
service_port: []
member_list:
  - host: []
    name: []
  - host: []
    name: []
  - host: []
    name: []

# Virtual Server Information
description: []
virtual_ip: []
vip_name: []
vip_service_port: []

Dependencies
------------

Your Ansible controller must include the ```f5networks.f5_modules```  collection to run this role. 

```bash
ansible-galaxy collection install f5networks.f5_modules
```

Example Playbook
----------------

- name: Create F5 LTM Rule
  hosts: localhost
  connection: local
  collections:
    - f5networks.f5_modules
  roles: 
    - f5-bigip

License
-------

BSD

Author Information
------------------
Author: Dhananja Kariyawam 
Blog: https://dhananjak.github.io/blogs/f5_bigip_automation_with_ansible/

