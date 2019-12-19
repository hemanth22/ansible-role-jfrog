Role Name: JFrog
=========

This ansible role will install jfrog in the aws ec2 using centos7 images.  

[![Build Status](https://travis-ci.org/hemanth22/ansible-role-jfrog.svg?branch=master)](https://travis-ci.org/hemanth22/ansible-role-jfrog)  

default Username: admin  
default Password: password  
default Port: 8081

Requirements
------------

You need to install python-pip and boto to launch this EC2 based ansible module.

Role Variables
--------------

Try exploring defaults/main.yml in the github to understand which variables can be override.

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
---
- hosts: localhost
  become: true
  gather_facts: false
  vars:
    keypair: Give your exiting keypair name here
    instance_type: give the instance_type
    security_group: Give your security group information
    vpc_subnet_id: give your vpc subnet id
    volume_size: Enter volume_size
    region: us-west-2 (CentOS image which i have chosen is working in us-west-2 better try this region)
    ec2_access_key: Give here aws_access_key
    ec2_secret_key: Give here aws_secret_key
  roles:
    - hemanth22.awx
```

License
-------

GPLv3

Author Information
------------------

This role was created in 2019 by Hemanth BITRA.
