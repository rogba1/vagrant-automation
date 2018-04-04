# Infrastructure automation using Vagrant and Ansible with Docker

## Background


This Vagrant profile uses Ansible to configure 2 VMs with Docker, then it uses Ansible to build and run three containers for Jenkins, SonarQube and Selenium server:

  - `Jenkins`: build server on an Ubuntu container.
  - `Selenium server`: Automated tests on an Ubuntu container.
  - `SonarQube`: Reporting analytics on an Ubuntu container.

## Getting Started

This README file is inside a root folder that contains a `Vagrantfile` which tells Vagrant how to set up your virtual machine in VirtualBox.

Prerequisites:

  1. Download and Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
  2. Download and Install [Vagrant](https://www.vagrantup.com/downloads.html)
  3. Install [Ansible](http://docs.ansible.com/ansible/latest/intro_installation.html)
  4. Open a shell prompt (Terminal app on a Mac) and cd into the folder containing the `Vagrantfile`
  

Once all of that is done, you can simply type in `vagrant up`, and Vagrant will create a new VM, install the base box, and configure it.

Once the new VMs are up and running (after `vagrant up` is complete and you're back at the command prompt), you can log into any VM via SSH if you'd like by typing in `vagrant ssh`.

