Droplet
=======

Creates a Digital Ocean droplet and adds the address to the group `droplets`.

Requirements
------------

This role uses the `digital_ocean` Ansible module which requires Python >= 2.6 with the `dopy` module on the executing host.

Role Variables
--------------

The following variables must be specified.

- `ssh_key_name` - The name of the SSH key to use. This may be a local key (found in ~/.ssh). If not, a new SSH key is generated.
- `droplet_name` - The name of the droplet. If the droplet does not already exist, it will be created.
- `api_token` - Your API token for the Digital Ocean API.

There are a number of other variables defined under `defauls` with reasonably sane default values. Any of these may be overridden, either in a playbook or on the command line.

- `ssh_key_password` - With default value "" (for no password).
- `image_id` - Which defaults to "ubuntu-16-04-x64".
- `size_id` - With default value "512mb".
- `region_id` - Set to "fra1" by default.
- `block_size` - Create and attach block storage volume of the given size. Set to 0 by default.

For the last three, refer to the Digital Ocean API [documentation](https://developers.digitalocean.com/documentation/v2/).

Example Playbook
----------------

The following example playbook creates a new Ubuntu Xenial droplet named `pikachu` in `nyc2`.

    - hosts: all
      roles:
         - role: fegge.droplet
           ssh_key_name: do-ssh-key
           droplet_name: pikachu
           api_token: a4fe0892...b0

License
-------

Unlicense (http://unlicense.org)

Build status
------------

[![Build Status](https://travis-ci.org/fegge/ansible-droplet.svg?branch=master)](https://travis-ci.org/fegge/ansible-droplet)
