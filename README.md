# ansible-role-ssh_known_hosts

Add sites to /etc/ssh/ssh_known_hosts for Debian/Ubuntu

## Prerequisites

First of all you should install [Ansible](http://www.ansible.com/home) on your machine, official [docs](http://docs.ansible.com/intro_installation.html) should help you with that.

# Installation
```bash
ansible-galaxy install igor_mukhin.ssh_known_hosts
```

## Example playbook

Lets make aliases for symfony2 console command

```yml
# playbook.yml

vars:
	ssh_known_hosts:
	  - github.com
	  - { host: bitbucket.org, type: rsa }

roles:
  - igor_mukhin.ssh_known_hosts

```
