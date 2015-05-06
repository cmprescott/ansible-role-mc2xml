Ansible Role: mc2xml
=========
[![Build Status][travis_badge]][travis_results]

Installs and configures [mc2xml][mc2xml].

Requirements
------------

mc2xml's author has made it non-trivial to download the bin via script. The author also left a polite note in the homepage's html asking to not download the bin via botting/scripting. To follow the author's wishes, download the [mc2xml][mc2xml] bin to the ansible host before running this role.

Role Variables
--------------

```yaml
mc2xml_bin_local: ~/Downloads/mc2xml      # path of downloaded bin on ansible host
mc2xml_bin_remote: /usr/local/bin/mc2xml  # path of bin on remote
mc2xml_path_output: /var/mc2xml           # dir to store mc2xml output
```

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

[mc2xml]: http://mc2xml.hosterbox.net/
[travis_badge]: https://travis-ci.org/cmprescott/ansible-role-mc2xml.svg?branch=master
[travis_results]: https://travis-ci.org/cmprescott/ansible-role-mc2xml