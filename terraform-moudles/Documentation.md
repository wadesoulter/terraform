# Deploying Two Instances In Two Regions On AWS Cloud Using Terraform




## Prerequisites
* : AWS Account: Ensure you have an AWS account. If you don't have one, you can sign up [here](https://aws.amazon.com)

* : Virtual Machine : a wide range of virtual machines can be used . From a virtual machine on virtual box to aws ec2 instance or a vm from your provider of choice .

* : Terraform Installation: Make sure you have Terraform installed on your local machine. You can download it from the [official website](https://www.terraform.) 


* : AWS CLI: Install the AWS CLI to configure your AWS credentials. You can download it here.


* : AWS Access Credentials: Obtain AWS Access Key ID and Secret Access Key. You can create one from the AWS Management Console.







### Terraform Configuration
* : Create a Terraform Configuration File:
Create a file named main.tf and add the following content:

provider "aws" {
  region     = "us-west-2"  # Update with your desired region
}

resource "aws_instance" "instance1" {
  ami           = "ami-0c55b159cbfafe1f0"  # Update with your desired AMI
  instance_type = "t2.micro"  # Update with your desired instance type
  count         = 1
}

* : Initialize Terraform:
command : terraform init

* : Deploy the Infrastructure:
command : terraform apply

* : Accessing Instances:
Once the deployment is complete, Terraform will output information about the created instances. Use this information to access your instances.


* : Run the following command to see the changes Terraform will make:
command: terraform plan -destroy

* : Execute the following command to destroy the instances:
command: terraform destroy
Confirm by typing yes when prompted.




# Please Note

* This basic documentation provides a starting point. Depending on your specific needs, you might want to add more configuration details, such as security groups, key pairs, or networking settings. Always refer to the official Terraform AWS provider documentation for more details and options.

* Depending on skill level , a basic understanding of Terraform and AWS is required for this task.






