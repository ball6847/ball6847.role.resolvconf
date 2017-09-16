Ansible Role : ball6847.role.resolvconf
==============================

Add nameserver entries to resolv.conf

Supported Operating System
--------------------------

Ubuntu

Installation
------------

```sh
ansible-galaxy install git+https://github.com/ball6847/ball6847.role.resolvconf.git,master
```

or by requirements.yml then do `ansible-galaxy install -r requirements.yml`

```yml
- src: https://github.com/ball6847/ball6847.role.resolvconf.git
  version: master
```

Playbook Example
----------------

```yml
# python.yml
- name: "Install python"
  hosts: all
  roles:
    - ball6847.role.resolvconf
```

Variables
---------

**resolv_nameserver**: `["8.8.8.8", "8.8.4.4"]`

List of nameserver to be appended to resolv.conf, default to Google Public DNS.

**resolv_file_location**: `/etc/resolvconf/resolv.conf.d/head`

Location of resolv.conf, default to `/etc/resolvconf/resolv.conf.d/head` which is a good place for ubuntu.
