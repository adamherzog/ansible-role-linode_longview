linode_longview
===============

Installs and configures Linode Longview monitor.

 * Sets up the Longview yum repository.
 * Configures the Longview client.
 * Optionally configures the longview client with MySQL credentials.
 * Installs and starts the Longview client.

Example Playbook
----------------

    - hosts: servers
      vars:
        linode_longview_api_key: 'api-key-goes-here'
        linode_longview_mysql_username: 'linode-longview'
        linode_longview_mysql_password: 'password-goes-here'
      roles:
         - linode_longview

Role Variables
--------------

 * linode_longview_api_key: null *required*

    Specify the Longview API Key for this server.

 * linode_longview_mysql_username: 
 * linode_longview_mysql_password: 

    Define the username and password Longview can use to monitor the MySQL
    server.

    This role *does not* add the user to MySQL; you must create the mysql
    account elsewhere.

Role Handlers
-------------

 * reload longview

