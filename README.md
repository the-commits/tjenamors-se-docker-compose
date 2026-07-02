[![sourcehut](https://img.shields.io/badge/sourcehut-~the--commits/tjenamors--se--docker--compose-2d6b9e?logo=sourcehut)](https://git.sr.ht/~the-commits/tjenamors-se-docker-compose)
[![GitHub mirror](https://img.shields.io/badge/GitHub-the--commits/tjenamors--se--docker--compose-181717?logo=github)](https://github.com/the-commits/tjenamors-se-docker-compose)

> **Do not open issues or pull requests on GitHub** — the mirror there is
> [read-only](https://git.sr.ht/~the-commits/tjenamors-se-docker-compose).
> Please use the [sourcehut issue tracker](https://todo.sr.ht/~the-commits/tjenamors-se-docker-compose)
> and send patches to [~the-commits/tjenamors-se-docker-compose@lists.sr.ht](mailto:~the-commits/tjenamors-se-docker-compose@lists.sr.ht).


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
