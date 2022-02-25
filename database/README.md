# Ansible Oracle Database Build

A simple example of an Oracle database build using Ansible.

This is just for fun. It's not supported, and I'm not accepting pull requests.


Place the Oracle software and patches in the "files" directory, as shown in the tree below.

```
├── ansible.cfg
├── database.yml
├── files
│   ├── LINUX.X64_193000_db_home.zip
│   ├── p33567270_190000_Linux-x86-64.zip
│   ├── p6880880_190000_Linux-x86-64.zip
│   └── put_software_here.txt
├── host_vars
│   └── database1.localdomain.yml
├── inventory.ini
├── README.md
└── roles
    ├── oracle_create_db
    │   └── tasks
    │       └── main.yml
    ├── oracle_create_service
    │   └── tasks
    │       └── main.yml
    ├── oracle_db_prereqs
    │   ├── tasks
    │   │   └── main.yml
    │   └── templates
    │       ├── dbora.service.j2
    │       ├── oracle_create_database.sh.j2
    │       ├── oracle_root_scripts.sh.j2
    │       ├── oracle_software_installation.sh.j2
    │       ├── oracle_software_patch.sh.j2
    │       ├── setEnv.sh.j2
    │       ├── start_all.sh.j2
    │       └── stop_all.sh.j2
    ├── oracle_os_prereqs
    │   └── tasks
    │       └── main.yml
    ├── oracle_root_scripts
    │   └── tasks
    │       └── main.yml
    ├── oracle_sw_install
    │   └── tasks
    │       └── main.yml
    └── oracle_sw_patch
        └── tasks
            └── main.yml
```
