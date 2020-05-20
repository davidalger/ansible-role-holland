# Ansible Role: Holland Backup Manager

[![Build Status](https://travis-ci.org/davidalger/ansible-role-holland.svg?branch=master)](https://travis-ci.org/davidalger/ansible-role-holland)

Installs the Holland Backup Manager for RHEL/CentOS and Fedora.

## Requirements

None.

## Role Variables

See defaults files under `defaults/main/` for descriptions and list of available variables for configuration templates.

## Dependencies

* `geerlingguy.repo-epel`

## Example Playbook

    - hosts: database
      roles:
        - davidalger.holland
      vars:
        holland_mysqldump_file_per_database: "yes"
        holland_mysqldump_compression_level: "3"
      tasks:
        - name: Configure Holland default backup set
          copy:
            dest: /etc/holland/backupsets/default.conf
            content: |
              [holland:backup]
              plugin = mysqldump
              backups-to-keep = 28
              purge-policy = after-backup
            mode: 0640

## License

MIT

## Author Information

This role was created in 2017 by [Ryan Chouinard](https://www.ryanchouinard.com/).
