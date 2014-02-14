LukeT.PostgreSQL
========

This role will install PostgreSQL with some minimal configuration, mostly benefits RHEL/CentOS users.



Requirements
------------

RHEL/CentOS
Debian/Ubuntu

Role Variables
--------------


_main.yml_ - 

```
auth_network: "192.168.42.0/32"
listen_address: "listen_addresses = 'localhost'"
pgsql_local_auth: "password"
pgsql_net_auth: "password"
```

_RedHat.yml_ - 

```
RedHat_server_pkgs:
  - postgresql
  - postgresql-server
  - postgresql-devel
  - python-psycopg2

pg_data_dir: '/var/lib/pgsql/data'
```

_Debian.yml_

```
Debian_server_pkgs:
  - postgresql-client-9.1
  - postgresql-9.1
  - postgresql-contrib
  - python-psycopg2
```

Dependencies
------------

None.

License
-------

BSD

Author Information
------------------

Luke Tislow
