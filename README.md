Role Name
=========

A role to install lustre client modules from a network share

Tested on EL7

Requirements
------------

Assumes you will build/obtain the module rpm's and place those to the given location beforehand.
Tested with Ansible 1.9.4 and 2.0.2.


Role Variables
--------------
```
lustre_lnet_networks: (default: none) -  what to put to /etc/modprobe.d/lustre.conf
lustre_mount_opts:    (default: _netdev,noatime,localflock,noauto) - Lustre mount options
lustre_mount_src:     (default: none) - Lustre mount source
lustre_mount_dir:     (default: none) - Path where Lustre will be mounted
lustre_packages:      (default: none)
  - <package>

lustre_network_devices: (default none) - which network devices should be brought up to make lustre work
  - <network device>
```
lustre_dir_mode: (default 0755) - mode for mount directory

Dependencies
------------

The role is written to be standalone


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansible-role-lustre_client }

License
-------

Apache License
Version 2.0, January 2004

Author Information
------------------
https://github.com/mhakala
https://github.com/jabl
