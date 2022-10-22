# terraform files to provision EC2 infrastructure on aws for the project

Usage:

Edit the credentials.tf file and add the AWS credentials

provider "aws" {
  region = "us-east-1"
  access_key = ""   <== fill this
  secret_key = ""   <== fill this
  #only needed for restricted accounts
  token = ""        <== optional, fill this only if you have a restricted account
}

#Create SSH key if you don't have one with the following command

ssh-keygen -t rsa -b 4096

#Initialize terraform

terraform init

#Have terraform validate your configuration

terraform validate

#Have terraform provision the AWS infrastructure

terraform apply -auto-approve

...... once done with the project ....

#Have terraform delete the provisioned AWS resources using the command below
terraform destroy -auto-approve
