# ANSIBLE-MYAWS REPO
Ansible repository for AWS Provisioning and Deployment.

## Prerequisite
Clone the repo on local system. Install the below packages on the

## Instruction
The hybrid-vpc module contains Ansible AWS Provisioning and deployment playbooks for hybrid vpc model.

All the Default configuration are defined in vars/defaults.yml file.
The only mandatory parameter thats needs to be updated is my_eip defined
in vars/vars.yml prior to the execution of any playbook.
Set the my_eip value to a valid Free Elastic IP associated with the AWS account.

Execute the ansible playbooks in the order defined below,

* ansible-playbook awsResources.yml --extra-vars "aws_secret_key=<secretkey> aws_access_key=<accesskey>"
* ansible-playbook webserver.yml
* ansible-playbook appserver.yml
