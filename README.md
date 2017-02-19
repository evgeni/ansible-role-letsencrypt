letsencrypt
===========

Ansible [Let's Encrypt](https://letsencrypt.org/) role, using [dehydrated](https://github.com/lukas2511/dehydrated).

[![Build Status](https://travis-ci.org/evgeni/ansible-role-letsencrypt.svg?branch=master)](https://travis-ci.org/evgeni/ansible-role-letsencrypt)

Requirements
------------

* Debian Jessie or newer
* NGINX (optional)

Role Variables
--------------

* `letsencrypt_user`: the user that will execute everything, default: `letsencrypt`
* `letsencrypt_basedir`: where to store certs and challenges, default: `/srv/letsencrypt`
* `letsencrypt_pk_renew`: whether to generate a new private key on every update, default: `no`
* `letsencrypt_domains`: which domains to request certs for, default: `[]`
* `letsencrypt_nginx`: enable NGINX integration, default: `false`

Dependencies
------------

None :-)

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: evgeni.letsencrypt }

License
-------

MIT/Expat

Author Information
------------------

Evgeni Golov <evgeni@golov.de>
