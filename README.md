Role Name
=========

Installs the [CodeIt repository](https://codeit.guru/en_US/) for RHEL/CentOS.

Requirements
------------

This role only is needed/runs on RHEL and its derivatives.

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

    codeit_repo_url: "https://repo.codeit.guru/codeit-repo-release.el{{ ansible_distribution_major_version }}.rpm"
    codeit_repo_gpg_key_url: "https://repo.codeit.guru/RPM-GPG-KEY-el{{ ansible_distribution_major_version }}"

The CodeIT repo URL and GPG key URL. Generally, these should not be changed, but if this role is out of date, or if you need a very specific version, these can both be overridden.

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
        - memiah.repo-epel

License
-------

MIT / BSD

Author Information
------------------

This role was created in 2022 by [Memiah Limited](https://github.com/memiah).

