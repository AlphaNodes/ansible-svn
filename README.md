# Ansible Role: svnserve service

Run svnserve on Debian and Ubuntu servers.

[![Ansible Galaxy](https://img.shields.io/badge/galaxy-alphanodes.svn-660198.svg)](https://galaxy.ansible.com/AlphaNodes/svn)
[![Build Status](https://travis-ci.org/AlphaNodes/ansible-svn.svg?branch=master)](https://travis-ci.org/AlphaNodes/ansible-svn)

## Dependencies

  none

## Installation

### Ansible 2+

Using ansible galaxy cli:

```bash
ansible-galaxy install alphanodes.svn
```

## Example Playbook

```yaml
- hosts: localhost
  roles:
    - AlphaNodes.svn
```

## License

GPL Version 3

## Author Information

This role was created in 2018 by [AlphaNodes](https://alphanodes.com/).
