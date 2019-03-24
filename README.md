# Ansible - Kong + Cassandra Playbook

## Infra

- Installs [Kong](https://konghq.com) and [Cassandra](http://cassandra.apache.org/) on a single node. Kong can be configured to use Cassandra as an external datastore. You can follow the [clustering guide](https://docs.konghq.com/1.0.x/clustering/) for more info.
The instances which needs to be monitored must have the following agents installed.

## Setup

- Clone the repo to your host machine

- Create a virtualenv to install Ansible

    `python3 -m venv venv`

    `source venv/bin/activate`

    `pip install ansible`

    Make sure Ansible is installed correctly and available in your PATH by running `ansible -v`

- Create an inventory file in your working directory, which is to be used with `ansible-playbook -i <inventory_file>` command. Refer to the sample format for [inventory](inventory.sample).

## Running the Playbook

`ansible-playbook setup.yml -i inventory -v --extra-vars="control_host={{hostname}} control_user={{user}}"`