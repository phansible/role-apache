# Phansible Role: Apache

[![Build Status](https://travis-ci.org/phansible/role-apache.svg?branch=master)](https://travis-ci.org/phansible/role-apache)

An Ansible Role that installs [Apache](http://httpd.apache.org/) on Ubuntu specifically created with [Phansible](http://phansible.com/) in mind.

## Requirements

// TODO

## Role Variables

The default role variables are located in `defaults/main.yml` and contain the information necessary to create Apache VirtualHosts. The `hosts` variable contains a list that allows a user to configure one or more VirtualHost(s).

`apache.hosts.docroot`: The Apache DocumentRoot of the VirtualHost you would like to create

`apache.hosts.servername`: The Apache ServerName of the VirtualHOst you would like to create

`apache.hosts.config_name`: The filename for the VirtualHost configuration file that will end up in `/etc/apache2/sites-enabled`. The default file name is `000-default.conf`, if you choose to configure multiple hosts, you must provide a different name to avoid continually overwriting the default VHost config.

## Dependencies

// TODO

## Example Playbook

// TODO

## License

This role is released under the terms of the license specified in the repository or if not specified, under the [MIT license](https://raw.githubusercontent.com/phansible/role-apache/master/LICENSE).

## Author Information

This role was created in 2015 by [The Phansible Team & Contributors](https://github.com/phansible/role-apache/graphs/contributors), credits go also to [Jeff Geerling](http://jeffgeerling.com/), author of [Ansible for DevOps](http://ansiblefordevops.com/) and source of inspiration.
