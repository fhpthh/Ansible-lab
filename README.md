# Ansible Lab — Hands-on Ansible Exercises

This repository contains a progressive set of **hands-on Ansible labs** (from `step-00` to `step-11`).  
Each step introduces a focused concept, example files (inventory, playbooks, roles), and short exercises to help you practice **Ansible fundamentals** and **more advanced topics**.

---

## Steps Overview

Below is a brief summary of each step directory and the concepts it covers.

- **step-00**: **Ansible Fundamentals**  
  Research-oriented introduction to core concepts and terminology (What is Ansible? Why use it? Key components).

- **step-01**: **Installing Ansible**  
  Platform-specific installation instructions (Ubuntu, Fedora) and verification steps.

- **step-02**: **Inventory**  
  Inventory structure, `ansible_host` and `ansible_user` variables, and connectivity testing using  
  `ansible -m ping`.

- **step-03**: **Ad-hoc Commands & Modules**  
  Using the `ansible` CLI with modules such as `shell`, `copy`, and `setup` for fact gathering and targeted commands.

- **step-04**: **Grouping Hosts**  
  Inventory group definitions, child groups, and organizing hosts for reusable targeting.

- **step-05**: **Playbooks**  
  Introduction to playbooks using an Apache example, including package installation with `apt` and playbook execution.

- **step-06**: **Playbook Refinements**  
  Enhancing playbooks to deploy virtual hosts, copy configuration files, and enable/disable sites using handlers.

- **step-07**: **Handlers & Service Restart Logic**  
  Restarting services only when configuration changes are valid.

- **step-08**: **Error Handling & Conditionals**  
  Configuration validation, registering task results, using `when`, `failed_when`, and `ignore_errors` to implement safe rollbacks.

- **step-09**: **Deploying a Website from Git Using Docker Built-in**  
  Cloning application code from Git, building/running containers, and deploying via Docker Compose.

- **step-10**: **Applying Standard Ansible Structure**  
  Refactoring the project to follow Ansible best practices using roles, `group_vars`, and `host_vars`.

- **step-11**: **Advanced: Applying HAProxy Load Balancer**  
  Deploying HAProxy with Ansible and verifying load balancing across backend services.

---

> **Note:**  
> Each step directory typically includes example inventories, playbooks, roles, and related files.  
> Open the corresponding folder and read its `README.md` for step-specific instructions and exercises.
