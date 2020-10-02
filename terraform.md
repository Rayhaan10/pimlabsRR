# Terraform
## Introduction
### What is terraform?
Terraform is a tool for **provisioning infrastructure** (or managing Infrastructure as Code). It supports multiple [providers](https://www.terraform.io/docs/providers/index.html) like **AWS, Google Cloud, Azure, OpenStack**..

### Getting Started
#### Installation

##### Windows

Installing Terraform is pretty straightforward, download it from the Terraform [download](https://www.terraform.io/downloads.html) page and select the appropriate package based on your operating system. The following [video](https://learn.hashicorp.com/terraform/getting-started/install.html) provides a good walk through of installing terraform. The installation steps from the video are outlined below.

The below steps is based off of version 0.12.13.

- Download [terraform](https://releases.hashicorp.com/terraform/0.12.13/terraform_0.12.13_linux_amd64.zip)
- Unzip it
```
$ unzip terraform_0.12.13_linux_amd64.zip
```
- Move the executeable file to `C:\Program Files (x86)`
- Add the binary to PATH environment variable:
  - In windows version 10 and above, go to Control Panel.
  - Click Advanced System settings. This option might vary in different versions of Windows.
  - The Advanced tab of the System Properties window is displayed.
  - Click Environment Variables near the bottom of the window.
  - The Environment Variables window is displayed.
  - In the System variables pane, click Path and then click Edit.
  - Click the _New_ button. Add the path to the folder where your Terraform executable is located.
  - Click OK to save your changes and then click OK to exit the Environment Variables windows. - Then click OK again to exit the System Properties window.
- To verify terraform is installed properly, type the following command in your command prompt window:
```
terraform version
```
the response should be
```
Terraform v0.12.13
```

##### Mac
These set of steps assume you have [brew](brew.sh) installed.
For Mac Users, type the following commands in terminal
```
brew intall git
brew install terraform
sudo cp terraform /usr/local/bin
sudo chmod +x /usr/local/bin/terraform
brew install awscli
aws configure
```

##### Linux
Terraform is distributed as a tarball on Github. Check the latest release on Terraform releases page before downloading below.
```
TER_VER=`curl -s https://api.github.com/repos/hashicorp/terraform/releases/latest | grep tag_name | cut -d: -f2 | tr -d \"\,\v | awk '{$1=$1};1'`
wget https://releases.hashicorp.com/terraform/${TER_VER}/terraform_${TER_VER}_linux_amd64.zip
```
Once the archive is downloaded, extract and move terraform binary file to a location within your PATH - typically `/usr/local/bin` directory. This will make the tool accessible to all user accounts.
```
$ unzip terraform_${TER_VER}_linux_amd64.zip
$ sudo mv terraform /usr/local/bin/
```
Check the version of Terraform installed
```
$ terraform --versions
```
Terraform v0.13.X

### Prerequisites
1. Existing AWS Account(OR Setup a new account)
1. IAM full access(OR at least have AmazonEC2FullAccess)
1. AWS Credentials(AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY)
1. Configure the Access keys and secret keys to AWS CLI
With all pre-requisites in place, it’s time to write your first terraform code.

### Overview

Terraform is a program developed by  **HashiCorp**. It uses what they call the _HashiCorp Configuration Language (HCL)_. It’s a **declarative language** where we define the type of infrastructure we want and terraform will figure out how to create it.

### Learning Paths
Here are links to some free resources where you can learn more about Terraform.
 - https://learn.hashicorp.com/collections/terraform/aws-get-started
 - https://www.thecloud.coach/courses/terraform-crash-course
 - https://hashicorp.wistia.com/projects/gs5p1ytajr
 - https://www.udemy.com/course/terraform-beginner-to-advanced/


### Hands-on Time:
The following exercises will help reinforce the learning that was done above:

#### Task 1:
Create a provider block and the resource EC2 instance block. Add the following arguments as part of the configuration code:
- Amazon Machine Image(AMI)
- Instance Type
- Tags

#### Task 2:
- Create an s3 bucket that is guaranteed to be globally unique. The
- Create multiple S3 buckets using a single resource. This should be done with count and with a for loop.

#### Task 3:
- Write TF code to create an ASG (autoscaling group) and a LC (launch configuration) to install the apache webserver.

##### Task 4
- Write TF move apache httpd configuration files over to S3 and then use user-data to pull the configuration down and restart apache.

### Terraform Certification
To get certified on Terraform, here are some useful links:
- [Hashicorp Associate Terraform Guide](https://learn.hashicorp.com/tutorials/terraform/associate-study)
- [Udemy Practice exam for Terraform Associate Exam](https://www.udemy.com/course/terraform-associate-practice-exam/)
- [250 Practice Questions For Terraform Associate Certification](https://medium.com/bb-tutorials-and-thoughts/250-practice-questions-for-terraform-associate-certification-7a3ccebe6a1a)
