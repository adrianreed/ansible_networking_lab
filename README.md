Description:
This playbook deploys a simple test environment to be used as a networking and linux services laboratory, consisting on one master host and one client host. This is for educational purposes only.

Requirements:
- Hosts run the following centOS image: CentOS 7 x86_64 Minimal 2009.
- Hosts run on the same network segment as the ansible controller, and have connectivity against each other.
- The ansible controller has SSH access to all hosts through root user with password. This is only used to create a standard user and grant passwordless SSH authentication and privilege escalation to root via sudo.

Usage:
1) Provision two centOS hosts.
2) Use the provided hosts.example file to build your '/etc/ansible/hosts' file.
3) Copy the provided group_vars/all file to '/etc/ansible/hosts/group_vars/all' and fill with the parameters you want for your environment.
4) Run the following ansible commands to build the laboratory:
```
# ansible-playbook deploy.yml --tags access -k
# ansible-playbook deploy.yml --tags base
# ansible-playbook deploy.yml --tags lab
```
