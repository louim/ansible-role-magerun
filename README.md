Role Name
=========

This role provide installation for [n98-magerun](https://github.com/netz98/n98-magerun).

Requirements
------------

The role itself doesn't depend on anything, but to be able to run Magerun, you will need to have PHP installed (and a full Magento compatible setup, too).

Role Variables
--------------

You can customize de the defaults used for Magento automatic installation. Those are the default value set by the role.

    magerun_installation_currency: USD
    magerun_installation_locale: en_US
    magerun_installation_timezone: America/New_York
    magerun_installation_use_secure: no
    magerun_installation_use_rewrites: yes
    magerun_installation_session_save: files
    magerun_installation_admin_username: admin
    magerun_installation_admin_firstname: John
    magerun_installation_admin_lastname: Doe
    magerun_installation_admin_password: magentodev
    magerun_installation_admin_frontname: admin
    magerun_installation_admin_email: john.doe@example.com

Dependencies
------------

None.

Example Playbook
----------------

Include the role in your playbook like so:

    - hosts: servers
      vars_files:
        - vars/main.yml
      roles:
        - { role: louim.magerun }

In your `vars/main.yml`, overwrite the variables you want:

    magerun_installation_currency: USD
    magerun_installation_locale: en_US
    magerun_installation_timezone: America/New_York
    ...

License
-------

MIT / BSD

Author Information
------------------

© [Louis-Michel Couture](https://twitter.com/louim) 2015
