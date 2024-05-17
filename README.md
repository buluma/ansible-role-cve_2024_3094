# Ansible role [cve_2024_3094](https://galaxy.ansible.com/ui/standalone/roles/buluma/cve_2024_3094/documentation)

Check xz vulnerability (cve_2024_3094) on your system.

|GitHub|Version|Issues|Pull Requests|Downloads|
|------|-------|------|-------------|---------|
|[![github](https://github.com/buluma/ansible-role-cve_2024_3094/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-cve_2024_3094/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-cve_2024_3094.svg)](https://github.com/buluma/ansible-role-cve_2024_3094/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-cve_2024_3094.svg)](https://github.com/buluma/ansible-role-cve_2024_3094/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-cve_2024_3094.svg)](https://github.com/buluma/ansible-role-cve_2024_3094/pulls/)|[![Ansible Role](https://img.shields.io/ansible/role/d/buluma/cve_2024_3094)](https://galaxy.ansible.com/ui/standalone/roles/buluma/cve_2024_3094/documentation)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-cve_2024_3094/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: true
  gather_facts: true

  roles:
    - role: buluma.cve_2024_3094
      cve_2024_3094_cleanup: false
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/buluma/ansible-role-cve_2024_3094/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: Prepare
  hosts: all
  become: true
  gather_facts: false

  roles:
    - role: buluma.bootstrap
    - role: buluma.openssh
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-cve_2024_3094/blob/master/defaults/main.yml):

```yaml
---
# defaults file for cve_2024_3094

# If requirements are installed, would you like to remove them after this role ran?
cve_2024_3094_cleanup: true

# Where to look for `sshd`, a list of paths.
cve_2024_3094_sshd_paths:
      - /usr/bin
      - /usr/sbin
      - /usr/local/bin
      - /usr/local/sbin
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-cve_2024_3094/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | Version |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Ansible Molecule](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-bootstrap.svg)](https://github.com/shadowwalker/ansible-role-bootstrap)|
|[buluma.openssh](https://galaxy.ansible.com/buluma/openssh)|[![Ansible Molecule](https://github.com/buluma/ansible-role-openssh/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-openssh/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-openssh.svg)](https://github.com/shadowwalker/ansible-role-openssh)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-cve_2024_3094/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[Alpine](https://hub.docker.com/r/buluma/alpine)|all|
|[Amazon](https://hub.docker.com/r/buluma/amazonlinux)|all|
|[Debian](https://hub.docker.com/r/buluma/debian)|bullseye|
|[EL](https://hub.docker.com/r/buluma/enterpriselinux)|all|
|[Fedora](https://hub.docker.com/r/buluma/fedora)|all|
|[opensuse](https://hub.docker.com/r/buluma/opensuse)|all|
|[Ubuntu](https://hub.docker.com/r/buluma/ubuntu)|focal, bionic, jammy|

The minimum version of Ansible required is 2.12, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-cve_2024_3094/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-cve_2024_3094/blob/master/CHANGELOG.md)

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-cve_2024_3094/blob/master/LICENSE)

## [Author Information](#author-information)

[Shadow Walker](https://buluma.github.io/)
