mysqlbix
=========

This role configures, and deploys the MySQLBix service which is used with Zabbix to gather database information.

Build Status
------------

[![Build Status](https://travis-ci.org/ericsysmin/ansible-role-mysqlbix.svg?branch=master)](https://travis-ci.org/ericsysmin/ansible-role-mysqlbix)

Requirements
------------

CentOS 7, EL 7 Supported Only at this time.

Role Variables
--------------

Please see the defaults/main.yml file.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - ericsysmin.mysqlbix
           zabbix_serverlist:
             - name: 'zabbixserver01'
               ip: '127.0.0.1'
               port: '10051'
           mysqlbix_databaselist:
             - name: db1
               database: db1
               dbhost: localhost
               port: 3304
               user: zabbix
               password: password
               querylistfile: ./conf/query.props

License
-------

GPLv2

Author Information
------------------

Eric Anderson ( ericsysmin.com )