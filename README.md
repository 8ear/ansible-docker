Ansible Docker Client Role
=====

This role installs and configures the Docker community edition engine.


## Requirements


This role requires Ansible 1.4 or higher and platform requirements are listed
in the metadata file.

## Role Variables

The variables that can be passed to this role and a brief description about
them are as follows.

    # The maximum concurrent downloads for `docker pull`
    max-concurrent-downloads: 50
    # The maximum concurrent uploads for `docker push`
    max-concurrent-uploads: 50
    # The log driver
    log-driver: "json-file"
    # The maximum file size of log driver 'json-file'
    max-size: "10m"
    # The maximum file count of log driver 'json-file'
    max-file: 5

## Examples

1) Install Docker deamon with defaults.

    - hosts: all
      roles:
      - {role: docker}

2) Install Docker deamon with syslog driver

    - hosts: all
      roles:
      - {role: docker,
         log-driver: syslog}


## Dependencies
None

## License
see [LICENSE file](LICENSE)

## Author Information

8ear