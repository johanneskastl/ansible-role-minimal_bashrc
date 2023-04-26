![Ansible Lint](https://github.com/johanneskastl/ansible-role-minimal_bashrc/workflows/Ansible%20Lint/badge.svg)

minimal_bashrc
=========

Create a minimal .bashrc

Requirements
------------

None.

Role Variables
--------------

- `additional_users`: (optional) Other users except the root user, that should
  get a ~/.bashrc. A good idea would be to create one for the `ansible_user`...
- `bashrc_for_root`: (optional) Boolean that decides if this role should create
  a `.bashrc` for the root user (default is `true`)

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: 'johanneskastl.minimal_bashrc'
          additional_users:
            - "{{ ansible_user }}"
            - 'alice'
            - 'bob'

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.
