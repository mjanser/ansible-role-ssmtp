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

### Recipient

All mails for user ids < 1000 will be rewritten to the address defined in the variable `ssmtp_recipient`.
If it's set to an empty string it will be disabled.

### Relay server

For sending mails you have to define a relay mail server in the variable `ssmtp_mailhub`.
If that server doesn't support TLS you can set `ssmtp_use_tls` to `no`.

Most mail servers require authentication for sending mails.
The credentials for this can be set in `ssmtp_auth_username` and `ssmtp_auth_password`.

## Dependencies

None

## Example Playbook

    - hosts: all
      roles:
        - { role: mjanser.ssmtp }

## License

MIT
