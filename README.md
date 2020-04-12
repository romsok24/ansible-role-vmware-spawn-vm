ansible-role-vmware-spawn-vm
=========

The ansible role for spawning a VM in the given vCenter

Requirements
------------
The role requires the below listed Pyton version and module to be installed on the Amsible host:
 - python >= 2.6
 - PyVmomi ( this requirement is fulfilled automatically by the role itself )
 
 Additionally, you need to place on the vCenter source template the powershell script for remote WinRM session entablement. 
 The script should be named _ConfigureRemotingForAnsible.ps1_ and placed in this path: _C:\Windows\temp\\_
 The script can be downloaded from https://github.com/ansible/ansible/blob/devel/examples/scripts/ConfigureRemotingForAnsible.ps1
The size of the source template is up to you. You can define ( in the defaults\main.yml ) the actual size of the destination VM and the role will automatically resize the disk for you.

Role Variables
--------------
All needed variables are defined and described in the _defaults\main.yml_ file


Known problems and limitations
--------------

* The role is not capable of IAM process so You need to take care of duplicate IP address avoidance topic


Author Contact Information
------------------

sok.r@wp.pl
