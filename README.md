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

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```
svn_server_packages:
  - subversion
```

Debian packages, which should be installed.

```
svn_server_user: svn
```

svn-serve will be run under the `svn_server_user`.

```
svn_server_group: svn
```

User group of `svn_server_user`.

```
svn_server_home: /srv/svn
```

Home directory of `svn_server_user`.

```
svn_server_repositories: '/srv/svn/repositories'
```

Directory for repositories (this should be within `svn_server_home` directory). In this directory all
repositories will be stored. Make sure you have enough disk space on used partition.

```
svn_server_user_password:
```

If you want to login with `svn_server_user` you can set a password.

```
svn_server_remove: no
```

To uninstall svnserve with all data, set `svn_server_remove` to yes.

```
svn_server_remove_packages: no
```

If you want to remove debian packages with  `svn_server_remove`, set `svn_server_remove_packages` to yes.



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
