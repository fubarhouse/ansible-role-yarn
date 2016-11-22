# Ansible Role: Yarn

[![Build Status](https://travis-ci.org/fubarhouse/ansible-role-yarn.svg?branch=master)](https://travis-ci.org/fubarhouse/ansible-role-yarn)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-fubarhouse--yarn-13698.svg)](https://galaxy.ansible.com/fubarhouse/yarn)

* Installs [Yarn](https://github.com/yarnpkg/yarn) for managing project dependencies.

## Requirements

  Yarn requires NodeJs v6+, and we recommend installing the role fubarhouse.nodejs prior to yarn. 

## Role Variables

To enable a clean install, set `yarn_clean_install` to True.
````
yarn_clean_install: False
````

To change which shell profiles are configured, change the following array to your needs:
````
yarn_shell_profiles:
  - .bash_profile
````

## Dependencies

  None.

## Example Playbook
````
- hosts: localhost
  roles:
    - fuabrhouse.nodejs # optional
    - fubarhouse.yarn
````

## License

MIT / BSD

## Author Information

This role was created in 2016 by [Karl Hepworth](https://twitter.com/fubarhouse).