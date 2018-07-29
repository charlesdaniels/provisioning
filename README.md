# Provisioning Scripts

[![Build Status](https://travis-ci.org/charlesdaniels/provisioning.svg?branch=master)](https://travis-ci.org/charlesdaniels/provisioning)

This is a collection of Ansible roles to set up machines for my personal use.

This playbook targets Debian Stable (currently Debian 9, Jessie). Some
roles may be more portable than others.

Any of the roles defined can be run against the local machine using this
command:

`ansible-playbook -K -i 127.0.0.1 -c local --tags desired_role ./site.yml`

The following roles are available:

* `common` - common base for all roles, includes dotfiles
* `workstation` - common base for all workstation type installations
* `laptop` - common base for all laptop type installations
* `x220` - provision ThinkPad X220 from the ground up

**NOTE**: You should run Ansible as the user account you log in with normally -
the `-K` will cause it to prompt you for the sudo password to use.
