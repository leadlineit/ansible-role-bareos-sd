# Ansible Galaxy role for install and configure Bareos Storage Daemon.

![Build Status](https://github.com/leadlineit/ansible-role-bareos-sd/actions/workflows/ansible-galaxy-ci.yml/badge.svg)

This role helps to install and configure Bareos Storage Daemon to Debian (buster/bullseye).

Requirements
------------

This role requires Ansible 2.9 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

```yaml
    bareos_sd:
      location:
        - path: /data/bareos
      director: 
        - name: your-dir
          password: DIRAver@gEStr0ngPaSSw0rd
        - name: your-mon
          password: MONAver@gEStr0ngPaSSw0rd
          monitor: "Yes"
          description: "Restricted Director monitor description"
      storage:
        - name: your.storage
      device:
        - name: your-data
          path: /data/bareos
          description: "Device description"
      messages:
        - name: your-messages
          server: your-dir
```

The variables above are optional. They don't have a default value, so if you don't define them - tasks using them will be skipped. 
You can set only some of them, or not set at all (in this case, you will simply install Bareos Storage with default configuration). 

Variable 'bareos_release' are optional.
Default values for optional variable:

```yaml
    bareos_release: 21
```

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
    - hosts: servers
      roles:
         - { role: leadlineit.bareos_sd, tags: bareos_sd }
```

License
-------

MIT

Author Information
------------------

This role was created by Artem Kasianchuk.
