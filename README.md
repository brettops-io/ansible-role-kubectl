# brettops.kubectl

[![pipeline status](https://gitlab.com/brettops/ansible/roles/kubectl/badges/main/pipeline.svg)](https://gitlab.com/brettops/ansible/roles/kubectl/-/commits/main)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)
[![ansible role](https://img.shields.io/ansible/role/61613)](https://galaxy.ansible.com/brettops/kubectl)
[![role downloads](https://img.shields.io/ansible/role/d/61613)](https://galaxy.ansible.com/brettops/kubectl)

An Ansible role to install
[`kubectl`](https://kubernetes.io/docs/tasks/tools/#kubectl) to a workstation.

Installing `kubectl` is not the hardest task in the world, but installing it
consistently and repeatedly across many platforms and enabling auto-completion
and symlinks and plugins and companion tools correctly is an accumulating
challenge.

This project is the first of a series of Ansible roles for solving these simple
challenges.

## What does this role provide?

This role does the following:

- Installs a stable version of `kubectl` to `/usr/local/bin/kubectl-X.Y`, where
  `X` and `Y` are the major and minor version numbers. It symlinks `kubectl` to
  this new installation, so that old `kubectl` versions remain available.

- Installs `kubens` and `kubectx` to simplify managing cluster contexts.

- Installs `k`, `kns`, and `kctx` symlinks to point to `kubectl`, `kubens`, and
  `kubectx`.

- Installs everything to `/usr/local/bin` to avoid interfering with the OS.

## Supported platforms

It is currently tested on the following platforms:

- Architectures: `x86_64` only

- Platforms:

  - Debian 11, 10, 9

  - Fedora 36

  - Ubuntu 22.04, 20.04, 18.04

## Installation

### From Ansible Galaxy

Add the following to your `requirements.yml` file:

```yaml
- name: brettops.kubectl
```

You can also use a specific version:

```yaml
- name: brettops.kubectl
  version: "0.1.0"
```

### From source

Add the following to your `requirements.yml` file:

```yaml
- name: brettops.kubectl
  src: git+https://gitlab.com/brettops/ansible/roles/kubectl.git
```

You can also use a specific version:

```yaml
- name: brettops.kubectl
  src: git+https://gitlab.com/brettops/ansible/roles/kubectl.git
  version: "0.1.0"
```

## Usage

Reference the role in your playbook:

```yaml
- hosts: all
  roles:
    - role: brettops.kubectl
```
