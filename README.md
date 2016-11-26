Ansible Role Mysql Admin
======================================

Ansible role to administrate mysql instances on gentoo instances.

Requirements
------------

None.

Role Variables
--------------

- `mysql_root_password`:
Password used for mysql root user.

- `mysql_databases`:
Array with mysql databases configuration. See
[default vars file](defaults/main.yml)

- `mysql_users`:
Array with mysql users configuration. See
[default vars file](defaults/main.yml)

Dependencies
------------

None.

Example Playbook
----------------
```
- hosts: all
  roles:
    - role: vundb-mysql-admin
      mysql_databases:
        - name: "example_db"
      mysql_users:
        - name: "example_user"
          pass: "example_pw"
          priv: "example_db.*:ALL"
```

License
-------

MIT

Author Information
------------------

- You can find more roles in my GitHub channel [vundb](https://github.com/vundb)
- Follow me on Twitter [@vundb](https://twitter.com/vundb)
