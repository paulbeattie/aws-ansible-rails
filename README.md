# Ansible Rails Server Setup

## Usage

You can run this Ansible Playbook using the following command and completing the parts specific to your setup.
This also includes setting users and host groups with site.yml as these may not be the same as you have.

```
ansible-playbook site.yml -i << your inventory file >> -l group
```

You also have the ability to skip some parts of the Playbook from running

```
ansible-playbook site.yml -i << your inventory file >> -l group --skip-tags "wkhtmltopdf"
```

## RVM role
This playbook uses the rvm1-ruby role, you will need to install this using Ansible Galaxy
```
ansible-galaxy install rvm_io.rvm1-ruby
```

## Redis
This playbook currently uses David Wittman's Ansible playbook for Redis.
This gives a much more modern version of Redis than the OS package manager.
You will need to install this using ansible-galaxy to use it.
```
ansible-galaxy install DavidWittman.redis
```

##
You need to create a new hosts file, this follows the following format:
```
[group_name]
111.111.111.111
```
