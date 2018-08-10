# ANSIBLE-MYAWS REPO
Ansible repository for AWS Provisioning and Deployment.

## Instruction
The hybrid-vpc module contains Ansible AWS Provisioning and deployment playbooks for hybrid vpc model.

All the Default configuration are defined in vars.yml file.
The only mandatory parameter thats needs to be updated is my_eip.
set the my_eip value prior to the execution of any playbooks to
a valid Free Elastic IP associated with the AWS account.
