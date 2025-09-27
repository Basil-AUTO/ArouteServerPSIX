# ArouteServerPSIX

---

## 2. Component Descriptions

| File/Folder | Purpose |
| :--- | :--- |
| **`inventory`** | The **Ansible Inventory** file, which lists all the target hosts (IXP routers/servers) where the configuration tasks will be run. |
| **`site.yml`** | The main **Ansible Playbook** file. This is the entry point that links the defined roles (`bird`, `openbgpd`) to the hosts specified in the inventory. |
| **`group_vars/all.yml`** | Contains global **variables** that are automatically applied to *all* hosts managed by the project. This is typically used for common settings like RPKI server addresses. |
| **`roles/`** | The core directory for **reusable automation components**. |
| **`roles/bird/`** | An Ansible role dedicated to configuring and managing the **BIRD** routing daemon. |
| **`roles/openbgpd/`** | An Ansible role dedicated to configuring and managing the **OpenBGPD** routing daemon. |
| **`tasks/main.yml`** | Defines the sequential list of **tasks** (e.g., installing the package, deploying the configuration file) for the respective role. |
| **`templates/*.j2`** | **Jinja2 templates** for configuration files (`bird.conf`, `bgpd.conf`). Ansible uses these to dynamically generate the final config file based on variables before deploying it to the target device. |
| **`handlers/main.yml`** | Defines actions (e.g., restarting the BIRD service) that are only executed when notified by a task, typically after a configuration change. |
