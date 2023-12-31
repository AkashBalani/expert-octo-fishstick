# expert-octo-fishstick

Why Ansible
1. IT automation tool to run automations
2. Ansible is an alternative to writing bash scripts
3. Imagine a case where you have a sequence to boot the vms, ansible can be helpful
4. Complex infra involving public and private cloud can be configured using ansible.
5. docs.ansible.com is useful.

Ansible Configuration Files
1. When you install ansible it creates a config file
2. /etc/ansible/ansible.cfg 
3. This file governs the default behavior of Ansible

Sections of ansible.cfg
1. [defaults] - most important section
- contains the default location of the config file, logs, modules or roles or plugins directory.
- whether ansible should be gathering facts by default for all executions.
- How long to wait before giving up on SSH connection attempt
- How many hosts ansible should target at a time when executing playbooks.
2. [inventory]
- Options for enabling certain inventory plugins
3. [privilege_escalation]
4. [paramiko_connection]
5. [ssh_connection]
6. [persistent_connection]
7. [colors]

Note: For every new environment you create in opt/env-name, you can add a ansible.cfg in it which can be referenced back in the original cfg file.

You can also change the location of the cfg file and then create an env variable.
ANSIBLE_CONFIG = /opt/ansible-web.cfg ansible-playbook playbook.yml

Priority
1. Env Variable
2. ansible file in the current directory
3. ansible file in the user directory (.ansible.cfg)
4. /etc/ansible/ansible.cfg

1. ansible-config list # Lists all configurations
2. ansible-config view # Shows the current config file
3. ansible-config dump # Shows the current settings
4. export ANSIBLE_

