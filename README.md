[![Build Status](https://travis-ci.org/open-io/ansible-role-openio-blackbox.svg?branch=master)](https://travis-ci.org/open-io/ansible-role-openio-blackbox)
# Ansible role `blackbox`

An Ansible role for deploying blackbox exporter (monitoring).

## Requirements

- Ansible 2.5+

## Role Variables


| Variable                         | Default                      | Comments (type)                   |
|:-------------------------------- |:---------------------------- |:--------------------------------- |
| `openio_blackbox_config_file`    | `/etc/blackbox_exporter.yml` | Path to blackbox config file      |
| `openio_blackbox_bind_interface` | -                            | Interface to listen on            |
| `openio_blackbox_bind_address`   | -                            | Address to listen on              |
| `openio_blackbox_bind_port`      | 9115                         | Port to listen on                 |
| `openio_blackbox_provision_only` | false                        | Provision only without restarting |

## Dependencies

No dependencies.

## Example Playbook

```yaml
- hosts: all
  become: true
  vars:
    NS: OPENIO
  roles:
    - role: users
    - role: blackbox
```


```ini
[all]
node1 ansible_host=192.168.1.173
```

## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section.

Pull requests are also very welcome.
The best way to submit a PR is by first creating a fork of this Github project, then creating a topic branch for the suggested change and pushing that branch to your own fork.
Github can then easily create a PR based on that branch.

## License

GNU AFFERO GENERAL PUBLIC LICENSE, Version 3

## Contributors

- [Vladimir DOMBROVSKI](https://github.com/vdombrovski) (maintainer)
- [Cedric DELGEHIER](https://github.com/cdelgehier) (maintainer)
- [Romain ACCIARI](https://github.com/racciari) (maintainer)
- [Vincent LEGOLL](https://github.com/vincent-legoll) (maintainer)
