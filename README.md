# # ansible-role-wireguard-exporter

Ansible role for deploying wireguard_exporter.

<img src="https://github.com/foi/ansible-role-wireguard-exporter/actions/workflows/ci.yml/badge.svg?branch=main">

Compatibility
--------------

python: 3.12, 3.13, 3.14
ansible: 12, 13, 14

prerequisites
--------------

docker and docker-compose should be installed.

Install
--------------

`ansible-galaxy role install foi.wireguard_exporter`

or add it in `requirements.yml`

```
roles:
  - name: foi.wireguard_exporter
```

and run `ansible-galaxy install -r requirements.yml`

Role Variables
--------------
role defaults:
```yml
wireguard_exporter_version: v0.3.0
wireguard_exporter_opts: []
wireguard_exporter_arch: x86_64
wireguard_exporter_user: wireguard-exporter
```

Example Playbook
----------------
```yml
# inventory
[wireguard]
server-1
# playbook.yml
- hosts: wireguard
  roles:
    - role: foi.wireguard_exporter
```
License
-------

MIT
