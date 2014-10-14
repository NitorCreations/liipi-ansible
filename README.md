Ansible playbook to create an AWS VPC environment.

Creates a new VPC and security groups inside it and some development environment instances. That's it for now.

Usage:

```
export AWS_ACCESS_KEY=<your key here>
export AWS_SECRET_KEY=<your key here>
ansible-playbook -i inventory/local site.yml
```

Game plan for bootstrapping full AWS infrastructure:

1. Running ansible externally (no AWS infrastructure exists yet), create the infrastructure, i.e. VPC, subnets, security groups.
2. Create an ansible instance (admin instance) inside the VPC. This host should have access to all entities managed with ansible (i.e. everything). Ansible is fully configured with all the necessary playbooks there. 
3. Further ansible playbooks (host internal config, deployment etc.) to be run from the ansible instance so we can have access to every instance etc.

