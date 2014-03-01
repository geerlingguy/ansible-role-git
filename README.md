# Ansible Role: Git

Installs Git, a distributed version control system, on any RHEL/CentOS Linux system.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `vars/main.yml`):

    git_packages:
      - git
      - git-svn

The specific Git packages that will be installed. By default, `git-svn` is included, but you can easily add this variable to your playbook's variables and remove `git-svn` if desired.

## Dependencies

None.

## Example Playbook

    - hosts: servers
      roles:
        - { role: geerlingguy.git }

## License

MIT / BSD

## Author Information

This role was created in 2014 by Jeff Geerling (@geerlingguy), author of Ansible for DevOps. You can find out more about the book at http://ansiblefordevops.com/, and learn about the author at http://jeffgeerling.com/.
