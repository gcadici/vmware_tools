# vmware_tools
Deploy the VMware Tools on Debian



A very simple cookbook to deploy vsphere vmware tools (officials) on Debian with Ansible.
This cookbook install all the necessary packages to run VMware tools, it mount a network sharing and unpack the vmware tools on your machine. Then, it executes the script which install the tools, and finally, clean all the temporary files and directories.

## Prerequisites

Before running the cookbook, you have to get back the tarball of the VMware Tools from Vsphere. 
Place it on a NAS and configure a network sharing.

In vSphere Client – Click Inventory > Virtual Machine > Guest > Install/Upgrade VMware Tools.See the [documentation](https://kb.vmware.com/s/article/2004754)
Then, mount the CDRom on your Virtual Machine and copy the tarball on your share.

## Usage

Don't forget to create your secret with ansible-vault
Launch vmware-tools playbook with Ansible

## Command

Example if you launch the command from the root of this directory :

`ansible-playbook playbook/vmware-tools.yml -K`
