# wordpress_ansible
Role Name
=========

#1. Provisioning

This role handles the initial setup of the server, including installing necessary packages, updating the package list, upgrading all packages, and configuring DNS settings.

Tasks:

    Install required packages.
    Run apt update and apt upgrade.
    Configure /etc/resolv.conf.

2. SSH Configuration

This role configures SSH settings by modifying the actual SSH configuration file. It includes changing the SSH port, disabling root login, and password authentication. It also manages user and group creation.

Tasks:

    Change SSH port.
    Disable root login.
    Disable password authentication.
    Create users and assign them to a group.
    Configure sudoers file for the group.

3. Nginx

This role installs Nginx, removes the default site configuration, and sets up a new site configuration.

Tasks:

    Install Nginx.
    Unlink default Nginx site.
    Deploy custom Nginx configuration.
    Enable the new site by creating a symlink in sites-enabled.
    Restart Nginx service.

4. PHP-FPM

This role installs PHP-FPM and necessary PHP modules, configures the www.conf file by modifying lines instead of copying templates, and restarts PHP-FPM.

Tasks:

    Install PHP-FPM and required modules.
    Configure www.conf.
    Restart PHP-FPM service.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
