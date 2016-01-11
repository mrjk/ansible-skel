# ansible-skel
This is my Ansible skeleton. It provide a nice structure to work comfortably with Ansible. You don't need to follow all principes of this structure to use Ansible.

This is a first draft of this structure, and it will evolve in the near future.

## File structure
The files structure is organised in this way:
```
.
├── config                                      # Configuration files
│   ├── ansible.cfg                                 # Ansible configuration
│   ├── init_ansible.yml                            # Playbook to download dependencies
│   ├── known_hosts                                 # Dedicated known host files
│   ├── README                      
│   ├── retry                                       # Retry directory
│   │   ├── arch.retry
│   │   └── controller_setup.retry
│   ├── ssh_config                                  # Dedicated SSH configuration
│   └── vault_password                              # Well, you know this this one ...
├── group_vars                                  # Group vars
│   ├── dev.yml                                     # Development group vars
│   ├── preprod.yml                                 # Preprod group vars
│   └── prod.yml                                    # Production group vars
├── inventory                                   # Inventory directory
│   ├── default.ini -> dev.ini                      # Symlink to default inventory
│   ├── dev.ini                                     # Development inventory 
│   ├── preprod.ini                                 # Preprod inventory
│   └── prod.ini                                    # Production inventory
├── LICENSE
├── playbooks                                   # Playbook directory (where you run ansible-playbook)
│   ├── ansible.cfg -> ../config/ansible.cfg        # Symlink to ansible.cfg
│   ├── arch.yml                                    # First playbook
│   ├── base.yml                                    # Second playbook
│   └── group_vars -> ../group_vars/                # Symlink to group_vars directory
│   └── host_vars -> ../host_vars/                  # Symlink to host_vars directory
├── plugins                                     # Plugins directory
│   ├── callback                                    # Callback plugins
│   │   ├── profile_tasks.py
│   │   └── profile_tasks.pyc
│   └── filter                                      # Filter plugins
│       ├── ipaddr.py
│       ├── ipaddr.pyc
│       ├── split.py
│       ├── split.pyc
│       ├── string_utils.py
│       └── string_utils.pyc
├── README.md                                   # You are currently reading me ... Yes, it's true
└── roles                                       # Top level role directory
    ├── local                                       # Local roles
    ├── profiles                                    # Profile roles
    ├── requirements.yml                            # Instruction to use external roles
    └── vendors                                     # Extenal roles
```





## Credits
There are a lot of goood ideas taken from the [enginyoyen ansible best practice repository](https://github.com/enginyoyen/ansible-best-practises/). The rest comes from some colleagues (Hi [Simon](https://github.com/spiette) !) and my customer experience.


