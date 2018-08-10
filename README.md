# ANSIBLE-MYAWS REPO
Ansible repository for AWS Provisioning and Deployment.

## Prerequisite
Clone the repo on local system from where you want to run ansible playbooks. Install the below packages,
* ansible
* python

Install the below python modules,
* boto
* boto3

## Instruction
The hybrid-vpc module contains Ansible AWS Provisioning and deployment playbooks for hybrid vpc model.

All the Default configuration are defined in vars/defaults.yml file.
The only mandatory parameter thats needs to be updated is my_eip defined
in vars/vars.yml prior to the execution of any playbook.
Set the my_eip value to a valid Free Elastic IP associated with the AWS account.

Edit the inventory file and update the webserver group section with
the Elastic IP used in the last step.


Execute the ansible playbooks in the order defined below,

* ansible-playbook awsResources.yml --extra-vars "aws_secret_key=secretkey aws_access_key=accesskey"
* ansible-playbook webserver.yml
* ansible-playbook appserver.yml

## Expected Outcome
The website is available over Elastic Public IP (DNS If Any).

https://ElasticIP
