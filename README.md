# Ansible Role: Git

Installs Git, a distributed version control system, on any RHEL/CentOS Linux system.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `vars/main.yml`):

    workspace: /root

Where certain files will be downloaded and adjusted prior to git installation, if needed.

    git_enablerepo: ""

This variable, a well as `git_packages`, will be used to install git via `yum` if `git_install_from_source` is false. Any additional repositories you have installed that you would like to use for a newer/different Git version.

    git_packages:
      - git
      - git-svn

The specific Git packages that will be installed. By default, `git-svn` is included, but you can easily add this variable to your playbook's variables and remove `git-svn` if desired.

    git_install_from_source: false
    git_install_path: "/usr"
    git_version: "1.8.4"

Whether to install Git from source; if set to `true`, `git_version` is required and will be used to install a particular version of git (see all available versions here: https://www.kernel.org/pub/software/scm/git/), and `git_install_path` defines where git should be installed.

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
