Ansible Role: MySQL Community 
=========

Ansible role to install MySQL on Linux

Requirements
------------

This role uses the mysql_native_password plugin and requires the following role variable to be passed in:

```aidl
mysql_root_passwd: new_root_password_here
```
Role Variables
--------------

Role will optionally configure databases when passed a dictionary in the following format:
```
application_databases:
    - db_name: database name
      db_archive: /path/to/archive.gz

application_database_users:
    - db_name: database name
      db_user: user name
      db_passwd: password
```
Dependencies
------------

None..

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: cyberitas.ansible_role_mysql }

License
-------

MIT

Author Information
------------------

Create in 2019 by James Dugger for Cyberitas Technologies, LLC
