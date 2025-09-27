# ArouteServerPSIX

psix-ixp-automation/
│── inventory
│── site.yml
│── group_vars/
│   └── all.yml
│── roles/
│   ├── bird/
│   │   ├── tasks/main.yml
│   │   ├── templates/bird.conf.j2
│   │   ├── templates/rpki_rtr_config.local.j2
│   │   └── handlers/main.yml
│   └── openbgpd/
│       ├── tasks/main.yml
│       ├── templates/bgpd.conf.j2
│       ├── templates/rpki_rtr_config.local.j2
│       └── handlers/main.yml
