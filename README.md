# Phansible Role: Apache

[![CI](https://github.com/phansible/role-apache/actions/workflows/ci.yml/badge.svg)](https://github.com/phansible/role-apache/actions/workflows/ci.yml)

An Ansible Role that installs [Apache](https://httpd.apache.org/) from the distribution packages with a default virtual host and common modules enabled, specifically created with [Phansible](http://phansible.com/) in mind.

## Requirements

- Ubuntu 22.04, 24.04, 26.04 or Debian 12, 13
- Ansible 2.15 or newer, with the `community.general` collection (shipped with the `ansible` package)

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
apache:
    docroot: "/vagrant"
    servername: "myApp.vb"
```

- `apache.docroot`: document root of the default virtual host, with `AllowOverride All`.
- `apache.servername`: `ServerName` of the default virtual host.

The role also enables `rewrite`, `vhost_alias`, `headers`, `expires` and `filter`, and sets `ServerSignature Off` and `ServerTokens Prod`.

## Dependencies

None.

## Example Playbook

```yaml
- hosts: all
  become: yes
  vars:
    apache:
      docroot: /var/www/app/public
      servername: app.test
  roles:
    - role-apache
```

## License

This role is released under the terms of the license specified in the repository or if not specified, under the [MIT license](https://raw.githubusercontent.com/phansible/role-apache/master/LICENSE).

## Author Information

This role was created in 2015 by [The Phansible Team & Contributors](https://github.com/phansible/role-apache/graphs/contributors), credits go also to [Jeff Geerling](http://jeffgeerling.com/), author of [Ansible for DevOps](http://ansiblefordevops.com/) and source of inspiration.
