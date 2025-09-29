Role Name
=========

Role to create 3 ec2 instances. 2 of them are ubuntu and 1 is linux.

Requirements
------------

If your terminal configured with aws cli, then we need not to provide access key and secret key. 

If not configured with aws cli, then we need to create a vault with a password.

command to create a simple password is 

openssl rand -base64 2048 > <filename.pass>

To create a vault

ansible-vault create <desired-vault-name.yml> --vault-password-file <filename.pass>


To execute playbook
------------

ansible-playbook <name-of-playbook.yaml>

if enabled vault

ansible-playbook <name-of-playbook.yaml> --vault-password-file <filename>

Example Playbook
----------------
Created role named as ec2. We use role name in playbook as below
---
- hosts: localhost
  connection: local

  roles:

     - ec2  # ec2 is the name of role


Author Information
------------------

I am venkat. 

I created this playbook as part of my learning
