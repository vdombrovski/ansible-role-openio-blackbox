[![Build Status](https://travis-ci.org/open-io/ansible-role-openio-blackbox.svg?branch=master)](https://travis-ci.org/open-io/ansible-role-openio-blackbox)
# Ansible role `blackbox`

An Ansible role for PURPOSE. Specifically, the responsibilities of this role are to:

-

## Requirements

- Ansible 2.4+

## Role Variables


| Variable   | Default | Comments (type)  |
| :---       | :---    | :---             |
| `openio_blackbox_...` | `...`   | ...              |

## Dependencies

No dependencies.

## Example Playbook

```yaml
- hosts: all
  become: true
  vars:
    NS: OPENIO

  roles:
    - role: repo
      openio_repository_products:
        sds:
          release: "18.10"
    - role: users
    - role: gridinit
      openio_gridinit_namespace: "{{ NS }}"
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
