Ansible Role: Authorized Keys
=========

Sync SSH keys from remote hosts to the Ansible controller. This is useful when redeploying
the host OS.

Requirements
------------

None

Role Variables
--------------

    # The remote user account to use for SSH connections. By default this role expects this value to be defined in ansible.cfg
    ansible_user: "apatt"

    # Remote user SSH password to use for initial connection
    ansible_password: "{{ vault_ansible_password }}"

Dependencies
------------

None

Example Playbook
----------------

    - name: Update SSH keys for Ansible controller known_hosts
      hosts: localhost
      connection: local
      gather_facts: false
      become: false

      roles:
        - jedimt.authorized_keys

License
-------

MIT

Author Information
------------------

Aaron Patten
aaronpatten@gmail.com
