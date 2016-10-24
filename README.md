Ansible Role: distcc
====================

[![Build Status](https://travis-ci.org/Anthony25/ansible-role-distcc.svg?branch=master)](https://travis-ci.org/Anthony25/ansible-role-distcc)

Ansible role to install distcc and distccd.

Role Variables
--------------

```yaml
# Should distcc be started at boot ? WARNING: put the boolean between quotes,
# as the result is used by a script on Ubuntu
distcc_start: "false"

# Networks/hosts allowed
distcc_allowed_nets:
  - "127.0.0.1"
  - "::1"

# Addresses to listen on
distcc_listener:
  - "127.0.0.1"
  - "::1"

# Nice lovel for distcc processes (leave it empty to use the default system
# value)
distcc_nice: 10

# Maximum jobs to accept (leave it empty to not set a limit)
distcc_jobs: ""

# Use zeroconf ? WARNING: put the boolean between quotes,
# as the result is used by a script on Ubuntu
distcc_zeroconf: "false"

# Hosts which will be saved in /etc/distcc/hosts
distcc_hosts:
  - "+zeroconf"
  - "127.0.0.1"
```

Dependencies
------------

None

License
-------

Tool under the BSD license. Do not hesitate to report bugs, ask me some
questions or do some pull request if you want to!
