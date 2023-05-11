Role Name
=========

draxalene.apache_php

Draxalene role for ansible to apache2, php-fpm, Memcached. (by hopla.cloud)

Requirements
------------

None.

Role Variables
--------------

System variables
user_name: "user"
user_email: "user@example.com"

Php variables
- php_version: "8.1"
- post_max_size: "64M"
- upload_max_filesize: "64M"
- short_open_tag: "On"

Memcached variables
- session_save_handler: "files"
- session_save_path: "/var/lib/php/sessions"

Dependencies
------------

- draxalene.linux_update
- draxalene.linux_motd


Example Playbook
----------------

    - hosts: localhost
      remote_user: root
      roles:
         - draxalene.apache_php

License
-------

GPLv3

Author Information
------------------

Alexandre MOREAU by hopla.cloud
