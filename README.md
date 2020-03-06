ansible-role-aliases
====================

[![Build
Status](https://travis-ci.org/alisio/ansible-role-aliases.svg?branch=master)](https://travis-ci.org/alisio/ansible-role-aliases)

Ansible Role - Add Aliases on RHEL/CentOS and Debian/Ubuntu.

## Alisio's Fork

I started started to maintain my own fork to integrate changes to the original lesmyrmidons.aliases repository faster.

This fork adds the following features on top of the original functionality:

* fix conditional os family check error
* Update deprecated privilege escalation method

## Requirements

None.

## Role Variables

		aliases_shell: zsh
		aliases_user: user
		aliases_aliases: []

## Example Playbook

    - hosts: all
      roles:
        - role: lesmyrmidons.aliases
          aliases_shell: bash
          aliases_user: vagrant
          aliases_aliases:
            - "alias ll='ls -la'"
            - "alias ping='ping -c4'"

## License

MIT / BSD
