OcO Ansible Role
=========

Install OcO package, clean it and configure it to run commands every minutes to check health

Role Variables
--------------

Checks list with name (no space) and command which output http standard response code (200, 302, ...)

oco_checks:
  - name: "google"
    command: "curl -o /dev/null --silent --head --write-out \"%{http_code}\" www.google.fr"

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
---
- hosts: all
  become: true
  vars:
    oco_checks:
      - name: "google"
        command: "curl -o /dev/null --silent --head --write-out \"%{http_code}\" www.google.fr"
  roles:
    - ansible-role-oco

License
-------


Author Information
------------------

STEAMULO - http://www.steamulo.com
