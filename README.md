linode_longview
===============

Installs and configures Linode Longview monitor.

 * Sets up the Longview yum repository.
 * Configures the Longview client.
 * Installs and starts the Longview client.

Example Playbook
----------------

    - hosts: servers
      vars:
        linode_longview_api_key: 'api-key-goes-here'
      roles:
         - linode_longview

Role Variables
--------------

 * linode_longview_api_key: null *required*

    Specify the Longview API Key for this server.

Role Handlers
-------------

none.
