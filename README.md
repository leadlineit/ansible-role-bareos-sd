# Ansible Galaxy role for install and configure Bareos Storage Daemon.

![Build Status](https://github.com/leadlineit/ansible-role-bareos-sd/actions/workflows/ansible-galaxy-ci.yml/badge.svg)

This role helps to install and configure MySQL Community Server 8.0 to Debian (buster/bullseye).

Requirements
------------

This role requires Ansible 2.9 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows.
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
         - { role: leadlineit.bareos-sd, tags: bareos-sd }
```

License
-------

MIT

Author Information
------------------

This role was created by Artem Kasianchuk.
