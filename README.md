# Configuration and change management

The code in the repo is meant to create a machine image on [AWS](https://amazon.com/aws) and provision the machine 
using ansible.
Packer is used for creating identical machine images on AWS in this case.

## Requirements
  - [Ansible](https://www.ansible.com)
  - [Packer](https://www.packer.io)

## Steps
To run the scripts first create `.env` fil
e, copy the contents of `.env.example` into `.env` file, fill in the placeholders 
in with details from aws account.
 - Run `source .env` to export the variable to the system environment.
 - Run  `packer build packer_frontend.json` to build the machine image.
 - Once done you should be able to go to your AWS account and create an instance from the image just created by packer.
