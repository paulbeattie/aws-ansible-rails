# Ansible Rails Server Setup

## RVM role
This playbook uses the rvm1-ruby role, you will need to install this using Ansible Galaxy
```
ansible-galaxy install rvm_io.rvm1-ruby
```

##
You need to create a new hosts file, this follows the following format:
```
[group_name]
111.111.111.111
```
