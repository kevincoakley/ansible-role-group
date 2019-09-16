ansible-role-group
==================

[![Build Status](https://travis-ci.org/kevincoakley/ansible-role-group.svg?branch=master)](https://travis-ci.org/kevincoakley/ansible-role-group)

Manage groups for CentOS 7, Ubuntu 18.04

Requirements
------------

None

Role Variables
--------------

See defaults/main.yml

Dependencies
------------

None

Example Playbook
----------------

    - name: Test the Group role for CentOS and Ubuntu systems
      hosts: group
      become: yes
      become_method: sudo
    
      vars:
        - group_list:
          - name: group01
            gid: 1001
          - name: group02
          - name: group03
            system: yes
          - name: group04
            state: absent
      roles:
        - ansible-role-group

License
-------

BSD

Author Information
------------------

Kevin Coakley (https://github.com/kevincoakley)
