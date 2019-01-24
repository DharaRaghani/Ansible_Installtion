# Ansible_Installtion on AWS EC2 instance. I am using Redhat Enterprise AMI.
Step 1: 
Launch 2 EC2 instances - Red Hat Enterprise Linux 7.6 (HVM), SSD Volume Type - ami-011b3ccf1bd6db744 (64-bit x86) / ami-0e3688b4a755ad736 (64-bit Arm)
Configure Security group and open the port 22 for SSH as Ansible doesn't require any agent. It can work with open SSH protocol.
Rename / Tag the instance one as Ansible-master and one as Ansible-slave. In order to get better understanding of your recurces please use apporiate TAGS.
Step 2:
SSH to Ansible-master instance using putty or MobaXterm tool. If you are using MobaXterm tool then you don't need to convert your keypair to ppk.
update the packages on launched instance using "yum install update -y" command. It's best practise to become root user while performing this action.
