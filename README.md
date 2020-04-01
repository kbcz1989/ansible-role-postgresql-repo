# Ansible Role: Install official postgresql repo

Installs postgresql official repositories on Debian, Ubuntu and CentOS/RedHat linux servers. More information can be found on [www.postgresql.org/download](https://www.postgresql.org/download/)

## Requirements

ansible 2.5+

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```

postgres_rpm_repo_url: 'https://download.postgresql.org/pub/repos/yum/reporpms/EL-{{ ansible_distribution_major_version }}-x86_64/pgdg-redhat-repo-latest.noarch.rpm'

postgres_repo_gpg_key_url: 'https://download.postgresql.org/pub/repos/yum/RPM-GPG-KEY-PGDG'

postgresql_apt_key: 'https://www.postgresql.org/media/keys/ACCC4CF8.asc'

postgresql_apt_repo_url: 'deb http://apt.postgresql.org/pub/repos/apt/ {{ ansible_distribution_release }}-pgdg main'

```

## Dependencies

None.

## Installation

```
$ ansible-galaxy install kbcz1989.ansible-role-postgresql-repo

Fedora repo can be added by defining the url in "postgres_rpm_repo_url"
```

## Example Playbook

    - hosts: server
      roles:
        - { role: kbcz1989.ansible-role-postgresql-repo }

## Supported OS

 - Debian 9 (Stretch)
 - Debian 8 (Jessie)
 - Ubuntu 18.04 (Bionic Beaver)
 - Ubuntu 16.04 (Xenial Xerus)
 - CentOS 6
 - CentOS 7
 - CentOS 8

## Required ansible version

Ansible 2.5+

## License

[MIT License](http://choosealicense.com/licenses/mit/)

## Author Information

 - [KBCZ1989]()
