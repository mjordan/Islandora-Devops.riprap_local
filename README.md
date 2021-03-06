## Overview

Ansible role that installs [Riprap](https://github.com/mjordan/riprap) and the [Islandora Riprap](https://github.com/mjordan/islandora_riprap) module in the [Islandora Playbook](https://github.com/Islandora-Devops/islandora-playbook). It also configures Islandora Riprap to perform fixity checks using Drupal's cron. It is intended to provide an easy-to-use installation of Riprap and Islandora Riprap for use on the VM more than for production use since running Riprap in local mode will likely not scale as high as running it on a separate server.

This role is based on https://github.com/roblib/Islandora-Devops.riprap from the University of Prince Edward Island. It differs from UPEI's role in that it installs Riprap in "local" mode and not as an HTTP microservice.

## Installation

1. In the `islandora-playbook/roles/external` directory, run `git clone https://github.com/mjordan/Islandora-Devops.riprap_local.git`
1. Open the `webserver.yml` file in the `islandora_-playbook` directory, and add `- Islandora-Devops.riprap_local` to the end of the list of roles. You can do this prior to running `vagrant up`, or, if you have already run that, you can run `vagrant provision` and Vagrant will add this role without redeploying other roles.

## Author

Mark Jordan (https://github.com/mjordan), based on the work of [Alan Stanley](https://github.com/ajstanley) and others at UPEI.

## License

MIT
