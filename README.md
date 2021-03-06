sensson.directadmin
=========

This module can be used to install DirectAdmin on CentOS-based servers. It
does not set an admin password so you would have to set this yourself once
the server is created or retrieve it from /var/log/directadmin/install.log.

It does not manage any configuration settings at the moment.

Requirements
------------

We assume you have a valid DirectAdmin license.

Role Variables
--------------

* `client_id`: The DirectAdmin client id.
* `license_id`: The DirectAdmin license id.
* `interface`: The server's interface. Default: eth0.

Dependencies
------------

None.

Example Playbook
----------------

```
- hosts: directadmin
  roles:
    - sensson.directadmin      
```

We recommend using host variables to set your client and license id. For
example:

```
[directadmin]
server.fqdn.com client_id=1000 license_id=10000
``` 

License
-------

GPLv3

Author Information
------------------

Sensson is a hosting company. We try to share our work whenever possible. We
do not intend to offer commercial support on our open source modules. We do 
welcome all pull requests though and will attempt to help whenever possible.
