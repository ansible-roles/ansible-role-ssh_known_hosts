# ansible-role-ssh_known_hosts
[![Build Status](https://travis-ci.org/ansible-roles/ansible-role-ssh_known_hosts.svg?branch=master)](https://travis-ci.org/ansible-roles/ansible-role-ssh_known_hosts)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-igor__mukhin.ssh__known__hosts-blue.svg?style=flat)](https://galaxy.ansible.com/list#/roles/3073)
[![Supported Platforms](http://img.shields.io/badge/platforms-ubuntu-orange.svg?style=flat)](#)
[![Ansible Version](http://img.shields.io/badge/ansible%20version-1.4+-lightgray.svg?style=flat)](#)

Add sites to /etc/ssh/ssh_known_hosts for Debian/Ubuntu

## Prerequisites

First of all you should install [Ansible](http://www.ansible.com/home) on your machine, official [docs](http://docs.ansible.com/intro_installation.html) should help you with that.

# Installation
```bash
ansible-galaxy install igor_mukhin.ssh_known_hosts
```

## Example playbook

Lets add github.com and bitbucket.org to known hosts:

```yml
# playbook.yml

vars:
	ssh_known_hosts:
	  - github.com
	  - { host: bitbucket.org, type: rsa }

roles:
  - igor_mukhin.ssh_known_hosts

```
