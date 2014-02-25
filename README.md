Kibana
========

[Kibana](https://github.com/elasticsearch/kibana) role for ansible.

A brief description of the role goes here.

Features
------------

* Protected with nginx and http basic auth
* Read-only access for data and read-write for dashboards
* Many instances per server could be deployed
* SSL ready, https is forced if enabled

Role Variables
--------------

* `kibana_owner` basically nginx user, `www-data` by default
* `kibana_git_url` git url for kibana, set to upstream by default
* `kibana_git_branch` git branch to track, set to master by default
* `kibana_root_path` path to clone kibana, `/var/www/kibana` by default
* `kibana_default_route` default dashboard url, `/dashboard/file/default.json` by default
* `kibana_index` kibana index to store dashboards, `kibana-int` by default
* `kibana_elasticsearch_url` elasticsearch url *for nginx*, http://127.0.0.1:9200 by default
* `kibana_nginx_config_name` nginx config name, `kibana.conf` by default
* `kibana_nginx_config_path` nginx configs dir, `/etc/nginx/sites-enabled` by default
* `kibana_nginx_listen` nginx listen address, `127.0.0.1` by default
* `kibana_nginx_server_name` nginx server_name (hostname), `127.0.0.1` by default
* `kibana_nginx_access_log` path to nginx access_log, `false` by default
* `kibana_nginx_error_log` path to nginx error_log, `false` by default
* `kibana_nginx_enable_ssl` whether or not ssl should be enabled, `false` by default
* `kibana_nginx_ssl_cert_path` nginx ssl certificate path, `""` by default
* `kibana_nginx_ssl_key_path` nginx ssl key path, `""` by default
* `kibana_nginx_http_auth_file` path to nginx http auth file, `false` by default

Miniman installation on ubuntu requires none of variables to be set, it will work on `http://127.0.0.1/`.

Dependencies
------------

It needs working nginx, elasticsearch and node.js to build kibana.

License
-------

MIT

Author Information
------------------

* Ian Babrou, ibobrik@gmail.com
