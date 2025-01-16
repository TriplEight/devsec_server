# Description

1. devsec playbook, links:
2. user and apps playbook
3. outline vpn playbook

## Requirements

for devsec: `ansible-galaxy collection install devsec.hardening`

for docker/portainer: `ansible-galaxy collection install community.docker`

## Setup

1. `cp example-inventory.yml inventory.yml`
  make sure to change the `example-inventory.yml` file to match your server's ip address and desired username
2. `ansible-playbook playbook_devsec_hardening.yml -i inventory.yml -u root --ask-become-pass`.
  After the `pre_steps` are successful, you should use your user because `root` will be denied at ssh login.


...
cloudflared
fish +