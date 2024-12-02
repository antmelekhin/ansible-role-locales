Locales
=======

An Ansible role to manage locales.

Requirements
------------

- Supported version of Ansible: 2.12 and higher. Systems with Python versions below than 3.7 are not compatible with ansible-core 2.17 (see [ansible/ansible#83357](https://github.com/ansible/ansible/issues/83357#issuecomment-2150254754)).
- Supported platforms:
  - Amazon Linux
    - 2
    - 2023
  - Debian
    - 10
    - 11
    - 12
  - Fedora
    - 39
    - 40
  - RHEL
    - 7
    - 8
    - 9
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

When using Ansible core, you will also need to install the following Ansible collections:

```yaml
---
collections:
  - name: community.general
```

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

Uninstall locales:

```yaml
---
- name: 'Uninstall locales'
  hosts: all

  roles:
    - role: antmelekhin.locales
      locales_absent_list:
        - 'en_US.UTF-8'
      when: ansible_os_family == 'Debian'

    - role: antmelekhin.locales
      locales_absent_list:
        - 'en_US.utf8'
      when: ansible_os_family == 'RedHat'
```

License
-------

MIT

Author Information
------------------

Melekhin Anton.
