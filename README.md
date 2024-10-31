# IaC using Terraform to create different resources in AWS

### For ease of managing resources its easier to separate your files based on the purpose they are serving.
 - An example is perhaps you need to create EC2 instances, VPC, security groups and many others will you really depend on one file(main.tf)? you can do it but we have modules which make it easy to have separation of concerns principle being applied.
 - What we can do is have modules folder and under that we can now create the folder for EC2, VPC etc.
 - After this will have a main.tf in the same directory with the modules folder where we will pass all our configurations referencing the created modules isn't that good?very nice.

### Using Input and Output variables
 - When creating an EC2 we need to have AMI and instead of hardcoding we just used input variables then when creating the resource we referenec the variable using "var" keyword.
 - For the instance type as well we do the same thing.
 - Since we are using IaC we don't need to keep on going to the management console to check on some things like ip address what we just do is utilizing the power of output variables.

### Set up the EC2 instance
 - So far there's a module for EC2 instance creation.

### Setup 
 - You neeed to have AWS CLI configured or else you can use GitHub codespaces though they have a limitation of 1 month.
 - Terraform should be installed on your machine.

### Terraform lifecylce commands
 - terraform init
 - terraform plan
 - terraform apply
 - terraform destroy
