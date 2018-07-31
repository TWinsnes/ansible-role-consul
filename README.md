# Ansible Role Consul

Role for deploying a consul cluster on long running servers.

## Supported OSes

This role has been tested on these OSes:

* RedHat Enterprise 7.5

## Role Variables

`application_group` group the user will be a member of

> Default: consul

`application_user` user to run consul as

> Default: consul

`application_version` version of consul to install. This is only used as part of the application download link, so this variable can be ignored if the download link is updated to not contain `{{ application_version }}`.

> Default: 1.2.1

`application_download_link` The path to download consul.

> Default: `"https://releases.hashicorp.com/consul/{{ application_version }}/consul_{{ application_version }}_linux_amd64.zip"`

`host_group_name` Name of the group in the inventory file containing the servers to run the role against. This is used to update the consul configuration file with all the servers in the cluster as part of the bootstrap process.

> Default: consuls