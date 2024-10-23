Locales
=======

An Ansible role to manage locales.

Requirements
------------

- Supported version of Ansible: 2.12 and highter.
- Supported platforms:
  - Debian
    - 10
    - 11
    - 12
  - Ubuntu
    - 18.04
    - 20.04
    - 22.04

Role Variables
--------------

All variables that can be overridden are stored in the [defaults/main.yml](https://github.com/antmelekhin/ansible-role-locales/blob/main/defaults/main.yml) file.
Please refer to the [meta/argument_specs.yml](https://github.com/antmelekhin/ansible-role-locales/blob/main/meta/argument_specs.yml) file for a description of the available variables.
Similarly, descriptions and defaults for preset variables can be found in the [vars/main.yml](https://github.com/antmelekhin/ansible-role-locales/blob/main/vars/main.yml) file.

Dependencies
------------

None.

Example Playbook
----------------

Manage locales:

```yaml
---
- name: 'Manage locales'
  hosts: all

  roles:
    - role: antmelekhin.locales
```

License
-------

MIT

Author Information
------------------

Melekhin Anton.
