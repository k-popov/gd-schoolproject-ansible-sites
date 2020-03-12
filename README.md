# Overview
This playbook allows to generate several locally available sites that would greet specific person by name.
Generated web-sites will be available by name in format `web-<name>` (entries added to `/etc/hosts`)

Built-in game is copied from https://github.com/wolverdude/asteroids

# Use
## Prerequirements
The following needs to be installed and configured:
- Ansible
- `python-docker` package
- Docker
## Running
`sudo ansible-playbook -i 127.0.0.1, -c local create_sites.yml`
`sudo` is required for Ansible could communicate with docker and update `/etc/hosts`
