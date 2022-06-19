ansible-role-mariadb
--------------------
Ansible role for deploying MySQL (MariaDB).


Role Variables
--------------

### Required Variables

The following variables are required (no defaults provided) and must always be
defined when using the role:

* `mysql_root_password`: The password for the default MySQL root user.

### Creation of Users and Databases

```
mysql_databases:
  - name: "database_name"
    encoding: utf8mb4
    collation: utf8mb4_unicode_ci
    mysql_users:
  - name: "{{ gitea_db_user }}"
    password: "{{ gitea_db_password }}"
    priv: "{{ gitea_db_name }}.*:ALL"
    update_password: on_create
```

### Optional Variables

See [defaults/main.yml](defaults/main.yml) for a list of optional variables.


Supported OS
------------
- Ubuntu 20.04
- Debian 10
- Debian 11
- Fedora 35
- ArchLinux


License
-------

MIT
