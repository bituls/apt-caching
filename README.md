Role Name
=========

Sets up apt so that it uses a caching proxy when installing packages. This just configures the apt tool so a server must be available and running the apt-cacher-ng tool.

Requirements
------------

You should have a running apt-cacher-ng server. See https://www.unix-ag.uni-kl.de/~bloch/acng/

https://github.com/bituls/ansible-container-caching-proxy can run it in a docker container

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

apt_cacher_host: Host of the apt caching server running apt-cacher-ng. E.g 127.0.0.1 (default)
apt_cacher_port: Port to the apt caching server. Default is 3142
apt_caching: Whether this role should enable caching for apt. Default is no. You must explicitly enable this which is useful for automated setups

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: bituls.apt-caching, apt_caching: yes }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
