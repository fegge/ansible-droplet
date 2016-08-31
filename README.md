Slack
=========

Deploy custom Slack webhooks to an Ubuntu server.

Requirements
------------

This role uses the `digital_ocean` module which requires Python >= 2.6 with the dopy module on the executing host.

Role Variables
--------------

- `admin_webhook` - Used by fegge.security to set up SSH logging to Slack.
- `piggelin_webhook` - Messages for the Piggelin channel will be posted here.
- `blackeberg_webhook` - Messages for the Blackeberg channel will be posted here.

All webhook URLs default to the empty string and must be set for the integrations to function properly.

Dependencies
------------

- fegge.security - Configures SSH logging, `ufw`, `fail2ban`, and `unattended-upgrades`.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: fegge.slack }

License
-------

Unlicense

Build status
------------

[![Build Status](https://travis-ci.org/fegge/ansible-slack.svg?branch=master)](https://travis-ci.org/fegge/ansible-slack)
