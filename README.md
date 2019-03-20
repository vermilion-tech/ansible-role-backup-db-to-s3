Backup DB to S3
=========
https://galaxy.ansible.com/vermilion_tech/ansible_role_backup_db_to_s3

Installs a docker service for creating database backups and sending them to S3.

Requirements
------------

Requires Python

Role Variables
--------------

`docker_install_compose` is set to `false`.
`pip.install_packages` installs `docker`, `docker-compose`, `boto3`, and `botocore`.

Dependencies
------------

See `vars/main.yml` for configurable options
- geerlingguy.docker
- geerlingguy.pip

Example Adhoc
-------------
```bash
$ ansible-role vermilion_tech.ansible_role_backup_db_to_s3 -i server.vermilion.tech, --hosts server.vermilion.tech --become --sudo
```

Example Playbook
----------------
`$ ansible-galaxy install vermilion_tech.ansible_role_ubuntu_base`

    - hosts: all
      roles:
         - { role: vermilion_tech.ansible_role_backup_db_to_s3 }

License
-------

BSD

Author Information
------------------

Kaden Nelson
`kaden@vermilion.tech`
vermilion.tech
