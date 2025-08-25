This the ansible playbook collection
=========

This repository includes 
  - Network management - Netplan configuration
  - Webserver management - Install, Configure Nginx
  - Openssh management  - Install Configure openssh, pubkey key management
  - Promtail - Install and configure promtail
  - Openldap - Install and configure both openldap server and client

Requirements
------------

Requirements for this ansible playbooks:
  - Ansible
  - Pre generater ssh key and tls certs for nginx
  - Your own ansible.cfg and inventory files

Roles
--------------

Roles included in this repository:
  - network - linux(ubuntu) network management 
  - nginx - includes role for nginx management
  - openldap - includes role for openldap management both server and client 
  - openssh - includes openssh config management
  - promtail - includes promtail deployment and configuration


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
  ```yaml
  - name: cofnig management
    hosts: all
    become: yes
    tasks:
      - name: Include nginx
        ansible.builtin.include_role:
          name: nginx
        tags:
          - tag
  ```

Important
-------
Variables and files(tls, sshkey, inventory, ansible.cfg  ... ) are not included here you need to define your own. Please dont commit anything that includes that files.

BSD

Author Information
------------------

This repository and playbooks developed by eMekdep Team. 
