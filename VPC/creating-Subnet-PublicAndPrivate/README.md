<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Build a Virtual Private Cloud

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-vpc)

**Author:** Muhammad Abdullah Dilshad  
**Email:** abdullahdilshad111@gmail.com

---

## Build a Virtual Private Cloud (VPC)

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-networks-vpc_2facf927)

---

## Introducing Today's Project!

In this project, I will demonstrate the Creation of the Vitual private Network (VPC) I'm doing this project to learn the basics of the Networking.

### What is Amazon VPC?

Amazon VPC is your private network inside AWS where you control IP ranges, subnets, and traffic flow.
It’s useful because it gives you full control over security and communication between your resources.
It lets you design public/private architectures (like internet-facing apps + secure backends) the way real systems are built.

In today's project, I used Amazon VPC to create my own VPC. In that vpc I created a public Subnet.Assigned CIDR blocks to all of them. And then made them accessable from the Internet Using the Internt Gateway.

### Personal reflection

This project took me 40 minutes;

One thing I didn't expect in this project was how easy we can do stuff through the Cloudshell.

---

## Virtual Private Clouds (VPCs)

### What I did in this step

In this step, I will access the VPC console from the Aws Management Console because the VPc can be setup from the VPC Console.

### How VPCs work

VPCs are called Virtual private Clouds more of like a cloud in Cloud. Its our Private space where we can store our resources, make our Networks private and Public and set permissions off who and what can access our resources, with or without the Internet Access.

### Why there is a default VPC in AWS accounts

There was already a default VPC in my account ever since my AWS account was created. This is because many service like Amazaon Ec2 needs a VPC to run in the Aws Account.

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-networks-vpc_2facf927)

### Defining IPv4 CIDR blocks

To set up my VPC, I had to define an IPv4 CIDR block, which is basically a zone or the range of my Ip Addresses.

---

## Subnets

### What I did in this step

In this step, I will setup a basic Subnet inside my VPC because in my VPC i dont want to place all my resources at a single place rather i want to divide the whole VPC into smaller Parts such as private Subnet and Private Subnet. Where i will place my Private resources in the private subnet and the public resources in the Public Subnet.

### Creating and configuring subnets

Subnets are indivisual networks inside the VPC. There are already subnets existing in my account, one for every Availability zone in that region

### Public vs private subnets

The difference between public and private subnets are that a public subnet has access to the Internet while a private Subnet does not have access to the Internet. For a subnet to be considered public, it has to be connected through an Internet gateway that basically acts as a bridge between the VPC and the Internet.

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-networks-vpc_157c4219)

### Auto-assigning public IPv4 addresses

Once I created my subnet, I enabled Auto Assign Public Ip Address .This setting makes sures that all the resources in my this subnet get a public IPv4 Address so that every resource must be accessed throuhg the interet when a Internet Gateway is Connected.

---

## Internet gateways

### What I did in this step

In this step, I will connect an Internet Gateway to my private subnet because i want to make this Subnet a public subnet and i want that all the resources in this Subnet must have a access to the Internet.

### Setting up internet gateways

An internet gateway connects your city (VPC) and the outside world (internet).

Internet gateways are key to making applications available on the internet. By attaching an internet gateway, your instances can access the internet and be accessible to external users.

Attaching an internet gateway to a VPC means I am provding the Subnet i am attaching this Internet Gateway to a way of having the internet access .If I missed this step My public subnet Would not have access to the Internet.

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-networks-vpc_4ae90410)

---

## Using the AWS CLI

### What I'm doing in this extension

In this project extension, I will Use the AWS Cloudshell to run commands because AWS Cloudshell will help us to setup the VPC and the subnets and the Internet Gateway in a supposed quicker way.

### Exploring CloudShell and CLI

VPC resources could also be created with CloudShell, which is a built in Aws Console to run the Aws Commands. CLI is Command Line Interface thats basically integerated in to the AWS Cloudshelll but if we are not using the Cloudshell, we will have to install that on our own laptop.

### Debugging my setup

To set up a VPC or a subnet, you can use the command

aws ec2 create-subnet --vpc-id vpc-0dcb12aa0d4282a4e --cidr-block 10.0.0.0/24

Make sure to avoid errors by including the Subnet Conflict

![Image](http://learn.nextwork.org/inspired_purple_radiant_bat/uploads/aws-networks-vpc_9b2465411)

### Comparing CloudShell vs AWS Console

Compared to using the AWS Console, an advantage of using commands is that its Fast.An advantage of using the Console is that its Fast Overall, I preferred Management Console For now.

---

---
