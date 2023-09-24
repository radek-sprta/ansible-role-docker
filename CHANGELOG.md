# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [3.0.1][3.0.1] - 2023-09-24

### Fixed

- Fixed docker-compose installation on Alpine.

## [3.0.0][3.0.0] - 2022-07-07

### Added 

- Support for Ubuntu 22.04.
- Validate arguments.

## [2.3.0][2.3.0] - 2022-03-15

### Added

- Add docker.socket as a managed service

## [2.2.0][2.2.0] - 2022-01-13

### Added

- `docker_daemon_options` to specify all of daemon.json.

### Deprecated

- The following options are now deprecated and will be removed in the future:
  - `docker_enable_metrics`
  - `docker_log_driver`
  - `docker_log_opts`
  - `docker_metrics_host`

## [2.1.0][2.1.0] - 2021-11-21

### Added

- Remove unused volumes in the scheduled maintenance job.

## [2.0.0][2.0.0] - 2021-08-27

### Fixed

- Append docker to user's groups instead of overwriting them.

### Removed

- Support for Ubuntu 16.04.

## [1.3.1][1.3.1] - 2021-01-31

### Fixed

- Format `docker_log_opts` as json.

## [1.3.0][1.3.0] - 2020-12-18

### Added

- Option to enable Prometheus metrics.

## [1.2.0][1.2.0] - 2020-11-07

### Added

- Support for Alpine Linux.

## [1.1.1][1.1.1] - 2020-09-17

### Fixed

- Ensure chosen Docker service state.

## [1.1.0][1.1.0] - 2020-09-16

### Added

- Make Docker package overwritable.

## 1.0.0 - 2020-09-07

### Added

- Role to install Docker and related tools.

[1.1.0]: https://gitlab.com/radek-sprta/ansible-role-docker/compare/v1.0.0...v1.1.0
[1.1.1]: https://gitlab.com/radek-sprta/ansible-role-docker/compare/v1.1.0...v1.1.1
[1.2.0]: https://gitlab.com/radek-sprta/ansible-role-docker/compare/v1.1.1...v1.2.0
[1.3.0]: https://gitlab.com/radek-sprta/ansible-role-docker/compare/v1.2.0...v1.3.0
[1.3.1]: https://gitlab.com/radek-sprta/ansible-role-docker/compare/v1.3.0...v1.3.1
[2.0.0]: https://gitlab.com/radek-sprta/ansible-role-docker/compare/v1.3.1...v2.0.0
[2.1.0]: https://gitlab.com/radek-sprta/ansible-role-docker/compare/v2.0.0...v2.1.0
[2.2.0]: https://gitlab.com/radek-sprta/ansible-role-docker/compare/v2.1.0...v2.2.0
[2.3.0]: https://gitlab.com/radek-sprta/ansible-role-docker/compare/v2.2.0...v2.3.0
[3.0.0]: https://gitlab.com/radek-sprta/ansible-role-docker/compare/v2.3.0...v3.0.0
[3.0.1]: https://gitlab.com/radek-sprta/ansible-role-docker/compare/v3.0.0...v3.0.1
