# Ansible Role: Yarn

[![Build Status](https://travis-ci.org/fubarhouse/ansible-role-yarn.svg?branch=master)](https://travis-ci.org/fubarhouse/ansible-role-yarn)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-fubarhouse--yarn-13698.svg)](https://galaxy.ansible.com/fubarhouse/yarn)

* Installs [Yarn](https://github.com/yarnpkg/yarn) for managing project dependencies.

## Requirements

  Yarn requires NodeJs v6+, and we recommend installing the role fubarhouse.nodejs prior to yarn. 

## Role Variables

To install global packages, use the `yarn_global_packages` array as described below.

****Note****: both `version` and `upgrade` are completely optional, but `name` is required. Set to `[]` to ignore this set of tasks.
 ````
yarn_global_packages:
- name: gulp 
  version: 3.9.0
  upgrade: yes
```` 

To run `yarn self-update <version>`, set the `yarn_version` variable.
````
yarn_version: 0.18.1
````

To enable a clean install, set `yarn_clean_install` to true.
````
yarn_clean_install: false
````

To specify a custom installation path for binaries, use:

***Note***: binaries will be found at location `{{ yarn_global_path }}/bin` 
````
yarn_global_path: /usr/local
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
    - fubarhouse.nodejs # optional
    - fubarhouse.yarn
````

## License

MIT / BSD

## Author Information

This role was created in 2016 by [Karl Hepworth](https://twitter.com/fubarhouse).