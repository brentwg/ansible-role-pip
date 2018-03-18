# Ansible Role: Python Pip
[![Build Status](https://travis-ci.org/brentwg/ansible-role-pip.svg?branch=master)](https://travis-ci.org/brentwg/ansible-role-pip)

This role installs Python Pip for Linux.

## Requirements  

None.  

## Role Variables 

Sane and opinionated defaults have been provided for installing Python Pip. See `defaults/main.yml` for more information.
```
pip_install_packages: []
```
List of additional Python Pip packages to install.

## Dependencies

None.  

## Sample Playbook
```
- hosts: all

  vars:
    pip_install_packages:
      # Test installing a specific version of a package.
      - name: ipaddress
        version: "1.0.18"
      # Test installing a package by name.
      - colorama

roles:
    - brentwg.pip
```
