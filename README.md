matthijsbos.aws\_s3
=========

[![Ansible Role](https://img.shields.io/ansible/role/17368.svg)](https://galaxy.ansible.com/matthijsbos/aws_s3/)
[![Travis](https://img.shields.io/travis/matthijsbos/ansible-role-aws-s3.svg)](https://travis-ci.org/matthijsbos/ansible-role-aws-s3)

Ansible role for downloading of files from amazon s3 using aws-cli as backend.

Requirements
------------

- [AWS CLI](https://aws.amazon.com/cli/) is to be installed on the remote host.

Installation
------------

Command line:
```
ansible-galaxy install matthijsbos.aws_s3
```

requirements.yml
```
# Ansible Galaxy, or
- src: matthijsbos.aws_s3
# Github
- src: git+https://github.com/matthijsbos/ansible-role-aws-s3
  name: matthijsbos.aws_s3
```

Role Variables
--------------

TODO: 
A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

TODO:
A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Download an object `test-file.txt` from bucket `test-bucket`.
```
- hosts: all
  roles:
      - role: matthijsbos.aws_s3
        aws_s3_src: s3://test-bucket/test-file.txt
        aws_s3_dest: /tmp/test.txt
        aws_s3_endpoint_url: http://minio:9000
        aws_s3_region: us-east-1
        aws_s3_access_key: AKIAIOSFODNN7EXAMPLE
        aws_s3_secret_key: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
```

License
-------

Apache License 2.0
