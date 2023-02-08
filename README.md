pgsql-backup
=========

Install and configure script for automated backups of PostgreSQL Databases https://github.com/fukawi2/pgsql-backup

Requirements
------------

Debian/Ubuntu only

Role Variables
--------------
```
pgsql_backup_dbhost: "localhost"
pgsql_backup_dbuser: "backup"
pgsql_backup_dbpassword: "StrongPassword"
pgsql_backup_destination_dir: "/mnt/backup/pgsql"
```

Dependencies
------------

None

Example Playbook
----------------

requirements.yml
```
---
roles:
  - src: https://github.com/sergeeximius/ansible-role-pgsql-backup.git
    scm: git
    name: sergeeximius.pgsql-backup
```

playbook.yml
```
---
- hosts: servers
  roles:
    - role: sergeeximius.pgsql-backup
```
License
-------

BSD

Author Information
------------------

Sergey Sedov serge.eximius@gmail.com
