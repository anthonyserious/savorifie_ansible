## Accountifie Deployment

Borrows liberally from https://github.com/ansible/ansible-examples and our friends at https://www.electronifie.com


- Requires Ansible 1.2 or newer
- Expects CentOS/RHEL 6.x hosts

These playbooks deploy a simple all-in-one configuration of a full accounting and reporting package, frontend by the Nginx web server with a django app and a node/mongo backend. To use, copy the `hosts.example` file to `hosts` and 
edit the `hosts` inventory file to include the names or URLs of the servers
you want to deploy.

Then run the playbook, like this:

	ansible-playbook -i hosts site.yml

The playbooks will configure PostgreSQL, Django, Nginx, mongo.