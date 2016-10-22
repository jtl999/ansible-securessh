SecureSSH
=========

An Ansible role to be run on a freshly installed server as the root user for locking down SSH and iptables

Testing on Debian 8.6 and Ubuntu 14.04 by me

How to use
==========

Edit vars/main.yml: `allowedip` to your current IP address (to be exempt from SSH brute force protection)

Review files/sshd_conf to ensure it meets your requirements

Define an Ansible playbook like this:

```
---
- hosts: testing
  roles:
          - securessh
```

(define your hosts somewhere I am new to using Ansible so I cannot help you at the moment)

Run it like this (as an example):

`ansible-playbook -s server.yml -i hosts.ini`