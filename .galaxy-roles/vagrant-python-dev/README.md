# ansible-role-vagrant-python-dev [![Build Status][travis.svg]][travis]

An Ansible role for a Vagrant-based Python development setup.

Available on Ansible Galaxy at [`naftulikay.vagrant-python-dev`][galaxy].

## Requirements

A Vagrant machine running a supported operating system.

## Role Variables

<dl>
  <dt><code>python_version</code></dt>
  <dd>The version of Python to install.</dd>
  <dt><code>vagrant_user</code></dt>
  <dd>The username of the Vagrant user, defaults to <code>vagrant</code></dd>
</dl>

> Please see the upstream [`naftulikay.vagrant-base`][vagrant-base] and [`naftulikay.python-dev`][python-dev] roles for
additional supported variables.

## Dependencies

 - [`naftulikay.vagrant-base`][vagrant-base]: Provides base Vagrant configuration.
 - [`naftulikay.python-dev`][python-dev]: Provides a basic Python development environment.

## Example Playbook

Install a Python development environment within the Vagrant machine:

```
---
- hosts: all
  roles:
    - role: vagrant-python-dev
      python_version: 2.7.13
```

## LICENSE

MIT.

 [travis]: https://travis-ci.org/naftulikay/ansible-role-vagrant-python-dev
 [travis.svg]: https://travis-ci.org/naftulikay/ansible-role-vagrant-python-dev.svg?branch=master
 [galaxy]: https://galaxy.ansible.com/naftulikay/vagrant-python-dev/
 [vagrant-base]: https://galaxy.ansible.com/naftulikay/vagrant-base/
 [python-dev]: https://galaxy.ansible.com/naftulikay/python-dev/
