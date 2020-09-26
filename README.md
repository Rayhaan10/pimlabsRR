# Curriculum

## Terraform
### Introduction
##### What is terraform?

Terraform is a tool for **provisioning infrastructure** (or managing Infrastructure as Code). It supports multiple providers(eg **AWS, Google Cloud, Azure, OpenStack**..).

https://www.terraform.io/docs/providers/index.html

### Getting Started on Terraform

##### Step 1: Installing Terraform and Download the Package on Windows system.

Installing Terraform is pretty straightforward, download it from **Terraform download page** and select the appropriate package based on your operating system.T watch the tutorial on installation , watch the first link .

https://learn.hashicorp.com/terraform/getting-started/install.html

https://www.terraform.io/downloads.html

https://releases.hashicorp.com/terraform/0.12.13/terraform_0.12.13_linux_amd64.zip

##### Step 2: Unzip it
```
$ unzip terraform_0.12.13_linux_amd64.zip
```
Download the applicable package to your local system.
Extract the package to the folder C:\Program Files (x86).

##### Step 3: Add the binary to PATH environment variable

1. This path is used as an example. However, you can also the Terraform executable to any other location in your local system.
2. Update the path environment variable to include the folder where your Terraform executable is located.
3. Go to the Control Panel.On a Windows 10 system, click Advanced system settings. This option might vary in different versions of Windows.
4. The Advanced tab of the System Properties window is displayed.Click Environment Variables near the bottom of the window.
5. The Environment Variables window is displayed.
In the System variables pane, click Path and then click Edit.
6. Click New. Add the path to the folder where your Terraform executable is located.
7. Click OK to save your changes and then click OK to exit the Environment Variables windows. Then click OK again to exit the System Properties window.


##### Step 4:  Verification
To verify terraform is installed properly, type the following command in CLI
```
$ terraform version
```
the response has to be
```
$ Terraform v0.12.13
```
### Install on Mac
For Mac Users, type the following commands in terminal
```
brew intall git
brew install terraform
sudo cp terraform /usr/local/bin
sudo chmod +x /usr/local/bin/terraform
brew install awscli\
awscli run configure
```
**How to Install Terraform on Linux**
Terraform is distributed as a tarball on Github. Check the latest release on Terraform releases page before downloading below.
```
TER_VER=`curl -s https://api.github.com/repos/hashicorp/terraform/releases/latest | grep tag_name | cut -d: -f2 | tr -d \"\,\v | awk '{$1=$1};1'`
wget https://releases.hashicorp.com/terraform/${TER_VER}/terraform_${TER_VER}_linux_amd64.zip
```
Once the archive is downloaded, extract and move terraform binary file to the /usr/local/bin directory.
```
$ unzip terraform_${TER_VER}_linux_amd64.zip
Archive:  terraform_xxx_linux_amd64.zip
 inflating: terraform

$ sudo mv terraform /usr/local/bin/
```
This will make the tool accessible to all user accounts.
```
$ which terraform
```
/usr/local/bin/terraform

Check the version of Terraform installed
```
$ terraform --versions
```
Terraform v0.13.X
To update Terraform on Linux, download the latest release and use the same process to extract and move binary file to location in your PATH.


#### Install ATOM  
atom.io\
A software development text editor. The closest competitors are VSCode, IntelliJ, and Eclipse (Not required).
#### Install atom packages
 file-icons\
 go-to-line\
 language-chef\
 linter-chefstyle\
 terraform-fmt

####Install Git - a popular version control system

Make a folder called Projects under My Documents
Make another folder called  Projects


##### Prerequisites
1. Existing AWS Account(OR Setup a new account)
2. IAM full access(OR at least have AmazonEC2FullAccess)
3. AWS Credentials(AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY)

4. Configure the Access keys and secret keys to AWS CLI
With all pre-requisites in place, it’s time to write your first terraform code.

#### Overview about Terraform Language

Terraform code is written in the **HashiCorp Configuration Language(HCL)**
All the code ends with the **extension of .tf**
It’s a **declarative language**(We need to define what infrastructure we want and terraform will figure out how to create it)


### Learning Paths
 #### Links to resources:
 - https://learn.hashicorp.com/collections/terraform/aws-get-started
 - https://www.udemy.com/course/terraform-beginner-to-advanced/
 - https://www.thecloud.coach/courses/terraform-crash-course
 - https://1drv.ms/v/s!Ali987OJCGh4hmfDlRvli1AA5jPw



### Hands-on Time:
##### Task 1:
Create a provider block and the resource EC2 instance block. Add the following arguments as part of the configuration code .
Amazon Machine Image(AMI)
Instance Type
Tags

##### Task 2:
a. Create a resource s3 bucket with a globally unique name\
b. Append your account id with S3 bucket to name the bucket\
c. Make 2 S3 buckets with count function\
d. Create a VPC, 2 subnets , IGW , route table in your network\
e. Create a security group with ingress ports open at port 22, 80 and 443\
f. Create an IAM user resource and attach permission policy ??\
g. Generate public , private key . Create a resource key pair and give the path of the public through file function\
h.Write terraform to launch a single instance with an output of the private ip\
i Launch two instances in terraform with individual resource blocks\
j.Launch two instances in terraform using a single resource block

##### Task 3:
Create an ASG (autoscaling group) and use LC (launch configuration) to install the webserver.\
Set the ASG to have minimum 2 instances.\
Terminate one of the instances, wait 0-2 minutes refresh, does a new instance come alive?

##### Task 4
Create s3 bucket and push the index.html file to the bucket from your local machine\
Modify the Launch configuration to pull index file out from the s3 bucket.


#### Exam Prep Guide
- Hasicorp Assosiate Terraform Guide
Terraform Study Guide

 https://learn.hashicorp.com/tutorials/terraform/associate-study

- Udemy Practice exam for Terraform Associate Exam

https://www.udemy.com/course/terraform-associate-practice-exam/


- 250 Practice Questions For Terraform Associate Certification\
https://medium.com/bb-tutorials-and-thoughts/250-practice-questions-for-terraform-associate-certification-7a3ccebe6a1a




## Bash Shell Scripting
### Introduction

**Bash**
Bash is a command language interpreter. It is widely available on various operating systems and is a default command interpreter on most GNU/Linux systems. The name is an acronym for the ‘Bourne-Again SHell’.

**Shell**
Shell is a macro processor which allows for an interactive or non-interactive command execution.

**Scripting**
Scripting allows for an automatic commands execution that would otherwise be executed interactively one-by-one.

#### Bash Scripting Tutorial
- https://www.youtube.com/playlist?list=PL7B7FA4E693D8E790\
(Complete list of 27 videos in playlist)

- https://www.udemy.com/course/bash-shell-scripting-crash-course-for-beginners/learn/lecture/9803252#questions/12581074


#### Guides
Here are some **web links** to try out!
- https://linuxconfig.org/bash-scripting-tutorial-for-beginners
- https://www.youtube.com/watch?v=IVquJh3DXUA
- https://www.codecademy.com/en/courses/learn-the-command-line
Vi - how to edit files when on a server in CLI mode




## Linux
#### Introduction
Linux is an **open source computer operating system,** initially developed on and for Intel x86-based personal computers. It has been subsequently ported to an astoundingly long list of other hardware platforms, from tiny embedded appliances to the world's largest supercomputers.

### History of Linux
**Linus Torvalds** was a student in Helsinki, Finland, in 1991, when he started a project: writing his own operating system kernel. He also collected together and/or developed the other essential ingredients required to construct an entire operating system with his kernel at the center. It wasn't long before this became known as the **Linux kernel.**

 By combining the kernel with other system components from the GNU project, numerous other developers created complete systems called **Linux distributions** in the mid-90’s.

 The **Linux distributions** created in the **mid-90s** provided the basis for fully free (in the sense of freedom, not zero cost) computing and became a driving force in the **open source software movement.** In 1998, major companies like IBM and Oracle announced their support for the Linux platform and began major development efforts as well.

 Today, Linux powers more than half of the servers on the Internet, the majority of smartphones (via the Android system, which is built on top of Linux), and all of the **world’s most powerful supercomputers.**

#### Free Online Linux Courses
https://hackr.io/blog/basic-linux-commands
https://learning.oreilly.com/videos/linux-fundamentals/9780135560396


#### Linux Commands Cheat sheet for Beginners
https://medium.com/faun/linux-commands-cheatsheet-for-beginners-1642169b2b7e




## AWS
### Introduction
AWS (Amazon Web Services) is a comprehensive, evolving **cloud computing platform** provided by Amazon that includes a mixture of **infrastructure as a service (IaaS), platform as a service (PaaS) and packaged software as a service (SaaS) offerings.** AWS services can offer an organization tools such as **compute power, database storage and content delivery services.**

AWS launched in **2006** from the internal infrastructure that Amazon.com built to handle its online retail operations. AWS was one of the first companies to introduce a **pay-as-you-go cloud computing model that scales to provide users with compute, storage or throughput as needed.**

#### Brief Overview of the Services provided by AWS

More than **100 services** comprise the Amazon Web Services portfolio. These services, by category, include:

- Compute
- Storage databases
- Data management
- Migration
- Hybrid Cloud
- Networking
- Development tools
- Management
- Monitoring
- Security
- Governance
- Big data management
- Analytics
- Artificial intelligence (AI)
- Mobile development
- Messages and notification



## Learning Path
Here are some links.
Now try this
1. **Adrian Cantril**
- https://learn.cantrill.io/p/aws-certified-solutions-architect-associate-saa-c02

2. Stephane Maarek
- https://www.udemy.com/course/aws-certified-solutions-architect-associate-saa-c02/

#### Exam Prep Resource and Cheat Sheets
1. **Tutorial Dojo**
- https://portal.tutorialsdojo.com/courses/aws-certified-solutions-architect-associate-practice-exams/

- https://tutorialsdojo.com/aws-cheat-sheets/

2. **Neal Davis**
- https://www.udemy.com/course/aws-certified-solutions-architect-associate-practice-tests-k/

- https://digitalcloud.training/certification-training/aws-solutions-architect-associate/


## GCP
### Introduction

Google Cloud Platform is essentially a **public cloud-based machine** whose services are delivered to customers on a **pay-as-you-go basis,** by way of service components.
A public cloud lets you leverage its resources to empower the applications you build, as well as to reach a broader base of customers.

#### Key Benefits
Google  Cloud’s security model provides **end-to-end process to clients’ data and application.**\
Google’s big data technology innovations provide innovative  services such as  
**BigQuery** for Data warehousing,\
**AI Platform** for advanced machine learning,
**Dataflow ,Pub/Sub, DataProc** for batch and real-time data processing,\
**Dataprep** for intelligent data preparation and Data studio provides powerful data insights.\
**Cloud big data analytics** solutions are serverless, removing the complexity of building and maintaining a data analytics system.\
**A Global Networking and edge caching** services to deliver fast, consistent, and scalable performance.
**Google Cloud data centers** run on half the energy of a typical data center, and run on 100% renewable energy where available.

## Guides to
Here are some links.
- https://linuxacademy.com/cp/modules/view/id/321

- https://www.coursera.org/learn/gcp-fundamentals#syllabus




## Git
### Introduction
#### What is Git?
Git is a **free, open-source version control software.** It was created by Linus Torvalds in 2005. This tool is a version control system that was initially developed to work with several developers on the Linux kernel.

This basically means that Git is a **content tracker.** So Git can be used to store content — and it is mostly used to store code because of the other features it provides.

#### How Git Works
Real life projects generally have multiple developers working in parallel. So they need a **version control system like Git** to make sure that there are no code conflicts between them.Also, the requirements in such projects change often. So a version control system allows developers to revert and **go back to an older version of their code.**


#### Git hosting services
There are three popular Git hosting services:

GitHub (owned by Microsoft), \
GitLab (owned by GitLab) and\
BitBucket.

##### Git Repositories
If we want to start using Git, we need to know where to host our repositories.

A repository (or “Repo” for short) is a **project that contains multiple files.** In our case a repository will contain code-based files.

##### Instal Git
1. Verify that Git is installed correctly by running the following command on the terminal

git --version

2. Run the following commands with your information to set a default username and email when you’re going to save your work.

git config --global user.name "MV Thanoshan"
git config --global user.email "example@mail.com"


#### Crash Course for Beginners
Here are some links to follow.
- https://www.youtube.com/watch?v=SWYqp7iY_Tc

- https://www.youtube.com/watch?v=Y9XZQO1n_7c

- https://www.freecodecamp.org/news/the-beginners-guide-to-git-github/

#### Basic Git Commands
- https://confluence.atlassian.com/bitbucketserver/basic-git-commands-776639767.html

#### Try it out
**Tasks:**
1. Create an account in Github.com
2. Create a repository via Github.com
3. Clone a repository via https and ssh (do you know what’s the difference ?)
4. Make changes to your code
5. Commit code
6. Push changes to origin
7. Create feature branch off of master
8. Submit pull request
9. Merge pull request
