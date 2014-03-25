# DevStack Vagrant

Ansible playbook to setup a DevStack environment using Vagrant.

### Dependencies

The following tools need to be in place for a working environment.

* VirtualBox
* Vagrant
* Ansible


### Environment

A Vagrant configuration file has been provided to setup an instance in VirtualBox. The Ansible playbook will perform the perform the initial setup of for the instance, followed by an installation of DevStack.

First, ensure that the permissions on the Vagrant private key are set correctly and launch the instance.

    $ chmod 600 Vagrant.pem
    $ vagrant up

Next, configure the Vagrant instance for development using Ansible. Be patient, the process could take a while to finish.

    $ ansible-playbook site.yml

Once configured, connect to the vagrant instance.

    $ vagrant ssh


### Platforms

Development has occurred on the following platforms:

* Ubuntu 12.04 (Precise)
