# kubectl Ansible role

[![pipeline status](https://gitlab.com/brettops/ansible/roles/kubectl/badges/main/pipeline.svg)](https://gitlab.com/brettops/ansible/roles/kubectl/-/commits/main)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)

An Ansible role to install kubectl on a machine.

## Usage

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
