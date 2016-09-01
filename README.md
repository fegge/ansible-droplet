Droplet
=======

Create a Digital Ocean droplet.

Requirements
------------

This role uses the `digital_ocean` Ansible module which requires Python >= 2.6 with the `dopy` module on the executing host.

Role Variables
--------------

- `ssh_key_name` - The name of the SSH key to use. This may be a local key (found in ~/.ssh). If not, a new SSH key is generated.
- `droplet_name` - The name of the droplet. If the droplet does not already exist, it will be created.
- `api_token` - Your API token for the Digital Ocean API.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: fegge.droplet }

License
-------

Unlicense

Build status
------------

[![Build Status](https://travis-ci.org/fegge/ansible-droplet.svg?branch=master)](https://travis-ci.org/fegge/ansible-droplet)
