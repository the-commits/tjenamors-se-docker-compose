# tjenamors-se-docker-compose

Ansible role for installing [Docker Compose](https://docs.docker.com/compose/).

## Requirements

- Docker Engine already installed
- Ansible 2.14+

## Installation

```bash
ansible-galaxy install tjenamors.docker_compose
```

Or add to `requirements.yml`:

```yaml
roles:
  - name: docker_compose
    src: git@git.sr.ht:~the-commits/tjenamors-se-docker-compose
    scm: git
    version: main
```

## Variables

| Variable | Default | Description |
|---|---|---|
| `docker_compose_install_method` | `plugin` | `plugin` (via apt) or `standalone` (binary) |
| `docker_compose_standalone_version` | `v2.34.0` | Version for standalone binary install |

## Example

```yaml
- hosts: all
  become: true
  roles:
    - role: docker_compose
```

## License

AGPL-3.0
