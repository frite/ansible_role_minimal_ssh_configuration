minimal_ssh_config
=========

Minimal SSH hardening for Ubuntu.


Role Variables
--------------

```
sshd_service_name: ssh
sshd_enabled: true
sshd_package_name: openssh-server

sshd_settings:
  "PasswordAuthentication": "no"
  "PermitRootLogin": "no"
  "PermitTunnel": "no"
  "Port": "22"

```
*IMPORTANT*
If the SSH Service is externally facing, move it to a higher port to keep spam low.

Example Playbook
----------------
```
    - hosts: servers
      roles:
         - { role: frite.minimal_ssh_config }
```
License
-------
MIT

Author Information
------------------
Manolis M.
