# Ansible Role: Holland Backup Manager

[![Build Status](https://travis-ci.com/davidalger/ansible-role-holland.svg?branch=master)](https://travis-ci.com/davidalger/ansible-role-holland)

Installs the Holland Backup Manager for RHEL/CentOS and Fedora with a default 7-day backupset configuration executed via a nightly cron job.

## Requirements

None.

## Role Variables

See defaults files under `defaults/main/` for descriptions and list of available variables for configuration templates.

## Dependencies

* `geerlingguy.repo-epel`

## Example Playbook

    - hosts: database
      roles:
        - { role: davidalger.holland, tags: holland }

## License

This work is licensed under the MIT license. See LICENSE file for details.

## Author Information

This role was created in 2017 by [Ryan Chouinard](https://www.ryanchouinard.com/) and extended by [David Alger](http://davidalger.com/).
