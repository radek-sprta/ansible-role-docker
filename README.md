# Ansible Role: Docker [![Ansible Role](https://img.shields.io/ansible/role/50554)](https://galaxy.ansible.com/radek_sprta/docker) [![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/radek-sprta/ansible-role-docker)](https://gitlab.com/radek-sprta/ansible-role-docker/-/tags) [![Ansible Role](https://img.shields.io/ansible/role/d/50554)](https://galaxy.ansible.com/radek_sprta/docker) [![Ansible Role](https://img.shields.io/ansible/quality/50554)](https://galaxy.ansible.com/radek_sprta/docker) [![Pipeline status](https://gitlab.com/radek-sprta/ansible-role-docker/badges/master/pipeline.svg)](https://gitlab.com/radek-sprta/ansible-role-docker/commits/master)

Install [Docker](https://www.docker.com) and optionally docker-compose and the Python docker library.

## Role Variables

### General options

- `docker_install`: Install Docker runtime. Defaults to true.
- `docker_install_compose`: Install docker-compose. Defaults to false.
- `docker_install_python_library`: Install docker python library. Defaults to false.
- `docker_package`: Name of the Docker package to install. Defaults to the appropriate system package.
- `docker_pip_package`: Name of the pip package to install. Defaults to the appropriate system package.

### Service options

- `docker_service_enabled`: Whether Docker should be enabled after restarted. Defaults to `true`.
- `docker_service_state`: State for the Docker service after installation. Defaults to `started`.

### Logging options

- `docker_log_drive`: Docker logging driver. Defaults to json-file (Docker default).
- `docker_log_opts`: Additional logging options. Pass as dictionary of Docker log-opts.

### Docker system prune

Automatically run `docker system prune`, so the system does not get cluttered with old images and containers.

- `docker_prune_period`: Filter `docker system prune` to images older than this variable. Defaults to `24h`.
- `docker_system_prune`: Whether to automatically run docker system prune. Defaults to `true`.

### Docker users

- `docker_users`: List of users that should be part of the docker group (thus able to control it). Defaults
  to `[]`.

## Example Playbook

```yaml
- hosts: all
  roles:
     - radek_sprta.docker
```

## License

MIT

## Author Information

Radek Sprta <mail@radeksprta.eu>
