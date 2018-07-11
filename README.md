mitogen
=========

[![Build Status](https://travis-ci.org/robertdebock/ansible-role-mitogen.svg?branch=master)](https://travis-ci.org/robertdebock/ansible-role-mitogen)

Mitogen is a Python library for writing distributed self-replicating programs.

Context
-------
This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://robertdebock.nl/) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/robertdebock/drawings/artifacts/ara.png "Dependency")

Requirements
------------

Access to a repository containing packages, likely on the internet.

Role Variables
--------------

None known.

Dependencies
------------

This role can be used to prepare your system:

- [robertdebock.bootstrap](https://travis-ci.org/robertdebock/ansible-role-bootstrap)
- [robertdebock.buildtools](https://travis-ci.org/robertdebock/ansible-role-buildtools)
- [robertdebock.epel](https://travis-ci.org/robertdebock/ansible-role-epel)
- [robertdebock.scl](https://travis-ci.org/robertdebock/ansible-role-scl)
- [robertdebock.python_pip](https://travis-ci.org/robertdebock/ansible-role-python_pip)

Download the dependencies by issuing this command:
```
ansible-galaxy install --role-file requirements.yml
```

Compatibility
-------------

This role has been tested against the following distributions and Ansible version:

|distribution|ansible 2.3|ansible 2.4|ansible 2.5|
|------------|-----------|-----------|-----------|
|alpine-latest|yes|yes|yes|
|alpine-edge|yes|yes|yes|
|archlinux|yes|yes|yes|
|centos-6|no|no|no|
|centos-latest|yes|yes|yes|
|debian-stable|yes|yes|yes|
|debian-latest|yes|yes|yes|
|debian-wheezy|yes|yes|yes|
|fedora-latest|yes|yes|yes|
|fedora-rawhide|yes|yes|yes|
|opensuse-leap|yes|yes|yes|
|opensuse-tumbleweed|yes|yes|yes|
|ubuntu-artful|yes|yes|yes|
|ubuntu-latest|yes|yes|yes|

Example Playbook
----------------

The simplest way possible:
```
- hosts: servers
  become: true

  roles:
    - robertdebock.bootstrap
    - robertdebock.epel
    - robertdebock.buildtools
    - robertdebock.scl
    - robertdebock.python_pip
    - robertdebock.mitogen
```

Install this role using `galaxy install robertdebock.ara`.

License
-------

Apache License, Version 2.0

Author Information
------------------

[Robert de Bock](https://robertdebock.nl/) <robert@meinit.nl>
