###### Description
This playbook deploys a simple test environment to be used as a networking and linux services laboratory, consisting on one master host and one client host. This is for educational purposes only.

###### Requirements
- Hosts run the following centOS image: CentOS 7 x86_64 Minimal 2009.
- Hosts run on the same network segment as the ansible controller, and have connectivity against each other.
- The ansible controller has SSH access to all hosts through root user with password.

###### Usage
- Provision two centOS hosts.
- Use the provided hosts.example file to build your '/etc/ansible/hosts' file.
- Copy the provided group_vars files to '/etc/ansible/hosts/group_vars/' and edit with the parameters you want for your environment.
- Run the following ansible commands to build the laboratory:
```
# ansible-playbook main.yml --tags access -k
# ansible-playbook main.yml --tags base
# ansible-playbook main.yml --tags lab
```
