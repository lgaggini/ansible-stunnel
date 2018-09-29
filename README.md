# ansible-stunnel

ansible-stunnel is an Ansible role to install and configure stunnel on a debian based OS.

It performs: 

* installation of stunnel package(s)
* configuration of tunnels
* creation of systemd unit, start and enable

## Install
### Clone
```bash
git clone https://github.com/lgaggini/ansible-stunnel
```
## Configuration

The configuration is done by vars listed and explained in [defaults/main.yml](https://github.com/lgaggini/ansible-stunnel/blob/master/defaults/main.yml) file.

## Usage

```
- name: bootstrap an ubuntu cloud image for dovecot
  hosts: mailserver
  vars_files:
    - group_vars/stunnel.yml

  roles:
    - { role: stunnel, tags: ['stunnel'] }
```
