# Ansible Role: ssmtp

An Ansible role that installs and configures ssmtp on Fedora.

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    ssmtp_recipient: postmaster
    ssmtp_mailhub: mail
    ssmtp_use_tls: yes
    ssmtp_auth_username: ~
    ssmtp_auth_password: ~

## Dependencies

None

## Example Playbook

    - hosts: all
      roles:
        - { role: mjanser.ssmtp }

## License

MIT
