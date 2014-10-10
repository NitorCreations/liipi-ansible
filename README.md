Ansible playbook to create an AWS VPC environment.

Creates a new VPC and security groups inside it. That's all for now.

Usage:

```
export AWS_ACCESS_KEY=<your key here>
export AWS_SECRET_KEY=<your key here>
ansible-playbook -i inventory/local site.yml
```