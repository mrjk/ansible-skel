# ansible-skel
This is my basic Ansible skel.


## File structure

.
├── config
│   ├── ansible.cfg
│   ├── ansible.log
│   ├── init_ansible.yml
│   ├── known_hosts
│   ├── README
│   ├── retry
│   │   ├── arch.retry
│   │   └── controller_setup.retry
│   ├── ssh_config
│   └── vault_password
├── group_vars
│   ├── dev.yml
│   ├── preprod.yml
│   └── prod.yml
├── inventory
│   ├── default.ini -> dev.ini
│   ├── dev.ini
│   ├── preprod.ini
│   └── prod.ini
├── LICENSE
├── playbooks
│   ├── ansible.cfg -> ../config/ansible.cfg
│   ├── arch.yml
│   ├── base.yml
│   └── group_vars -> ../group_vars/
├── plugins
│   ├── callback
│   │   ├── profile_tasks.py
│   │   └── profile_tasks.pyc
│   └── filter
│       ├── ipaddr.py
│       ├── ipaddr.pyc
│       ├── split.py
│       ├── split.pyc
│       ├── string_utils.py
│       └── string_utils.pyc
├── README.md
└── roles
    ├── local
    ├── profiles
    ├── requirements.yml
    └── vendors

