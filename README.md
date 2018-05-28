# terraform-rpm
This simple Ansible playbook creates and installs an RPM package of the current release of Hashicorp's Terraform.

By default, it will download, RPMize and install the current version of Terraform, but by specifying the variable `version`, on the command line, you can have an arbitrary version packageized and installed.

If the version that you build is newer than what you have installed, it will be automatically upgraded.

## Usage

[source, bash]
----
ansible-playbook main.yml -K [ --extra-vars "version=<desired version>" ]
----
