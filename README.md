﻿# gpcapstone3
This code repository is for AWS infrastaructure creation using terraform.

There are 5 files which are involved in terraform infra creation.

**provider.tf** :- Defines AWS region, puts the tfstate file into already created S3 bucket.
**vpc.tf** :- Creates 3-tier network which consists of below.
4 subnets (two public, two private). 
two AZs. 
one IGW 
one NAT.
Route tables (one default, one public and one private).

RDS was created manually for the project.

**sg.tf** :- creates one public and one private SG.
**key.tf** :- maps the public key to EC2 instances for SSH purposes. Private key is used while accessing the EC2 instances.
**ec2.tf** :- creates 3 instances - one App instance for WORDPRESS APP, one Bastion instance, and one Jenkins instance.


**WORDPRESS App code repository link** - https://github.com/f7tozap/gpcapstone3code.git
