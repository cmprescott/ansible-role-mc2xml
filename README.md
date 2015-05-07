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
# ENV configuration
mc2xml_bin_local: ~/Downloads/mc2xml        # path of downloaded bin on ansible host
mc2xml_bin_remote: /usr/local/bin/mc2xml    # path of bin on remote
mc2xml_lineup_num: 3                        # local provider to select from choices get by running mc2xml
mc2xml_path_output: /var/mc2xml             # dir to store mc2xml output

# MANDATORY configuration
mc2xml_geo_country_code: "US"               # country code to lookup providers
mc2xml_geo_postal_code: "90210"             # zip/postal code to lookup providers

# OPTIONAL configuration (set to include)
mc2xml_channel_offset: "<#>"                # add <#> to all channel numbers
mc2xml_duration: "<#>"                      # set listings duration (in hours)
mc2xml_file_ren: "mc2xml.ren"               # set ren filename
mc2xml_file_dat: "mc2xml.dat"               # set dat filename
mc2xml_file_channel: "mc2xml.chl"           # set channel file
mc2xml_file_xmltv: "xmltv.xml"              # set output file
mc2xml_include_xmltv: "<filename>"          # include <xmltv file> in output
mc2xml_rel_start: "<[+/-]#>"                # set listings relative start position (in hours )
mc2xml_titantv_id: "<id>"                   # set 30 char id for titantv service
mc2xml_sched_direct_creds: "<user>:<pass>"  # use schedules direct service
mc2xml_wait: "<#>"                          # wait for <seconds> and exit

# OPTIONAL params (override to Yes to include)
mc2xml_channel_name: No                     # output channel "name" first (rather than "number name")
mc2xml_force_re_dl: No                      # force re-download (use responsibly)
mc2xml_include_live: No                     #                      include <live /> tag (not part of xmltv.dtd)
mc2xml_mark_new: No                         # append " *" to new programs
mc2xml_mark_live: No                        # append " *" to live programs
mc2xml_mark_old: No                         # append " *" to not new programs
mc2xml_titantv: No                          # use titantv service
mc2xml_UTC: No                              # output date/time in UTC (default = localtime)
mc2xml_UTF_8: No                            # output UTF-8 (default = "ISO-8859-1")
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