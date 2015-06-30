# ansible_recipes

This repository aims to present some playbooks for creating, provisionning, destroying and upgrading a digital ocean droplet.

## inventory
All playbooks need a "webservers" group.

## playbooks
* do_create_and_configure
* do_destroy
* do_upgrade

## roles
* ntp : install ntp package from ubuntu repository
* nodejs : install latest nodejs version from official nodejs ppa
* apache2 : install latest apache2 version from ubuntu repository
* passenger : install latest passenger version from official passenger ppa
* ufw : configure standard ufw (allow 22 and 443 only)

## Todo
* split first part of do_create_and_configure in multiple roles
* add configurations variables for ufw
* add option to disable 000-default in apache2 role

## Warning
Because of a race condition, I am not able to permit to create multiple nodes at once (only one node is acceptable in "webservers" group)
