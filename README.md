#A solution using Cloudformation template and Ansible to automate the installation of basic WordPress. 


A cloudformation template that accepts user inputs as parameters. This template setup VPC, create subnets, launch a CM instance, and configure the web  Wordpress setup.

Run the Ansible playbook to create the stack and the local `wordpress` inventory file:

    $ ansible-playbook create.yml -i aws

You will be prompted for the EC2 key pair ID that you wish to use for access to the EC2 instance after it is created. This must be the ID of the keypair you will use in the command below.

To provision the WordPress site, please run below and supply the key file for EC2 access:

    $ ansible-playbook provision.yml -i wordpress --private-key=/path/to/ec2/key.pem
# InfrastructureAsCode
