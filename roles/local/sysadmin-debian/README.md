Sysadmin role for Ansible
=========

A brief description of the role goes here.
This role will update the system, install some useful packages and push a nice bashrc configuration.

Requirements
------------

You only need ansible ( tested with 1.9.4 ), and CentOS or Debian hosts. You can pretty simply add support for your own distribution.

Role Variables
--------------

There are the default variables:
sysadmin_sysupdate: no
  Set to yes if you want to do a full upgrade of the OS
sysadmin_debian_pkgs: []
  An array of package to install on Debian based systems
sysadmin_centos_pkgs: []
  An array of package to install on CentOS based systems

You can easily add the support of your distribution, by adding a file in the /vars directory.

Dependencies
------------

There is no dependency on this role.

Example Playbook
----------------

Here is a playbook example:

- hosts: all
  user: root
  roles:
  - sysadmin

License
-------

GNU GENERAL PUBLIC LICENSE
Version 2, June 1991

Copyright (C) 1989, 1991 Free Software Foundation, Inc., <http://fsf.org/>
51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA
Everyone is permitted to copy and distribute verbatim copies
of this license document, but changing it is not allowed.


Author Information
------------------

I'm here: jeznet.org, say me hello if you want :)

