Docker Role
=========

This role install Docker and Docker-bundles for Linux Debian based and Mac based system (using Brew)

Requirements
------------

- Linux Debian based system
- MacOS based system
- Ansible
- Brew (for MacOS)

Role Variables
--------------

NaN

Dependencies
------------

NaN

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

Build ByDefault.

Test
----

``ansible-playbook tests/test.yml -i tests/inventory --syntax-check``

ToDo
----

- RHEL/Fedora Support