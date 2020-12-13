# ansible-tomcat

### Install ansible in Amazon Linux2
  sudo amazon-linux-extras install ansible2

### Set environment variables
  export AWS_ACCESS_KEY_ID='<AWS ACCESS KEY>' </br>
  export AWS_SECRET_ACCESS_KEY='<AWS SECRET ACCESS KEY>'

### List of aws ec2 instances in groups
  ansible-inventory -i aws_ec2.yml --graph </br>
  ansible-inventory -i aws_ec2.yml --list

### Execute ansible playbook to install, configure and deploy tomcat and war file 
  ansible-playbook -i aws_ec2.yml site.yml -e "ansible_user=ec2-user passed_in_hosts=tag_my_app_asg"
  
# Terraform

### change to terraform directory
cd terraform
### Initialize terraform (download's provider [AWS] packages)
terraform init
 
### Create the terraform plan
terraform plan
 
### Create the resources, type yes when prompted (creates a VPC named myvpc in AWS)
terraform apply
