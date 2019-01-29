# Ansible redis role

Role for Ansible which installs Redis and Redis-Sentinel in clustered state. At this point in time, this role supports only CentOS 7.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Ansible >= 2.5

```
This needs to be installed on the deployment machine running Ansible, not on the target hosts.
```

### Recomendations

3-node setup at minimum since we want to reach our Redis quorum and have proper switching between Redis masters.

### Deployment

This is a very simple role for Redis and Redis-Sentinel. Basically, you will need to do something like this when you have your prerequisites installed:

```
ansible-playbook -i <inventory_file> playbooks/redis.yml
```

A playbook is not included in this role since this varies from setup to setup, but here is an example one:

```
---

- hosts: redis
  roles:
    - redis
```

## Built With

* [Ansible 2.5](https://docs.ansible.com/ansible/latest/roadmap/ROADMAP_2_5.html) - The main tool used for auto-deployment.

* **Valentin Dzhorov** - *Initial work* - [Github](https://github.com/vdzhorov/redis-ansible)

## License

This project is licensed under the GNU General Public License v3.0
