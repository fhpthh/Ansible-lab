# Ansible: Running with a Standard Project Structure

Ansible projects should follow a standard directory structure (skeleton) to ensure clarity, reusability, and maintainability.

```
project_folder_name/
├── inventory/
│   ├── hosts
│   ├── group_vars/
│   │   └── all.yml
│   └── host_vars/
│       └── web01.yml
├── roles/
│   └── service-01/
│       ├── tasks/
│       │   └── main.yml
│       ├── handlers/
│       │   └── main.yml
│       ├── templates/
│       ├── files/
│       └── vars/
│           └── main.yml
├── playbooks/
│   └── site.yml
└── ansible.cfg
```

## Key Components Explained

### Inventory

- `hosts`: Defines host groups and target machines.
- `group_vars`: Variables shared by a group of hosts.
- `host_vars`: Variables specific to individual hosts.

### Roles

Roles organize automation logic in a reusable way.

Each role typically contains:

- tasks/ → main automation logic.
- handlers/ → restart/reload services.
- templates/ → Jinja2 templates.
- files/ → static files.
- vars/ → role-specific variables.

### Playbooks

Playbooks define which roles run on which hosts.

Example site.yml:

```
---
- name: Deploy service
  hosts: web
  become: true
  roles:
    - service-01
```

_Note_:
Because I do not want to expose passwords in YAML files, I use Ansible Vault to encrypt all VM passwords and store them securely in a vault file.
These encrypted passwords are then used by Ansible as the value of ansible_become_pass during privilege escalation.

Encrypted vault file

```
ansible-vault create group_vars/all/vault.yml
```

```
# group_vars/all/vault.yml (encrypted)
ansible_become_pass: "S3cr3tP@ssw0rd"
```

```
# group_vars/all.yml
ansible_become: true
```

Running the playbook

```
ansible-playbook site.yml --ask-vault-pass
```

or using a vault password file:

```
ansible-playbook site.yml --vault-password-file ~/.vault_pass.txt
```
