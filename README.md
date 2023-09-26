# Writing Good Documentation

## Step 1 - Using Terraform.

- Terraform is Infra-as-Code tool make it *very easy* for tech people to *copy, paste share* the code.
A Good __Cloud Engineer__ uses Codeblocks whenever possible.

- Because it allows others to copy and paste their code to replicate or research issues.
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")
```
# Define the provider (AWS in this case)
provider "aws" {
  region = "us-west-2" # Specify your desired AWS region
}

# Define an EC2 instance resource
resource "aws_instance" "example_instance" {
  ami           = "ami-0c55b159cbfafe1f0" # Specify the AMI ID for your desired OS
  instance_type = "t2.micro"              # Specify the instance type
  key_name      = "your-key-pair"         # Specify the name of your SSH key pair
  subnet_id     = "subnet-0123456789abcdef0" # Specify the subnet ID

  tags = {
    Name = "ExampleInstance"
  }
}

# Define an output to display the public IP address of the instance
output "instance_public_ip" {
  value = aws_instance.example_instance.public_ip
}
```
- This Terraform code accomplishes the following:

-  Specifies the AWS provider with the desired AWS region.

  Defines an EC2 instance resource called "example_instance" with specific configuration options such as the Amazon Machine Image (AMI), instance type, SSH key pair, and subnet ID.

  Adds a tag to the instance for easy identification.

  Defines an output that displays the public IP address of the created instance.

Make sure to replace the placeholder values (e.g., AMI ID, key pair name, subnet ID) with your specific AWS configuration. To use this code, you'll need to have Terraform installed, configure your AWS credentials, and run terraform init and terraform apply in the directory where the code is located.

This is a simple example, and Terraform can be used to manage more complex infrastructure setups, including networks, security groups, databases, and more. You can extend this example by adding more resources and configurations to suit your infrastructure needs.
- [ ] Finished Step 1
- [ ] Finished Step 2
- [ ] Finished Step 3
# Step 4 - Use Emojis (Optional)
| Name | Shortcode | Emoji
| ---|---|---|
|Cloud| `:cloud:` |:cloud:|

# Reference Links
- https://www.terraform.io/
- https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#images
