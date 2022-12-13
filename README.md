Role Name
=========

Installs the [CodeIT repository](https://codeit.guru/en_US/) for RHEL/CentOS.

Requirements
------------

This role only is needed/runs on RHEL and its derivatives.

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

    codeit_repo_major_version: "{{ ansible_distribution_major_version }}"
    
    codeit_repo_gpg_key_url: "https://repo.codeit.guru/RPM-GPG-KEY-el{{ codeit_repo_major_version }}"
    
    codeit_repo_file_name: "codeit-el{{ codeit_repo_major_version }}"
    codeit_repo_file_path: "/etc/yum.repos.d/{{ codeit_repo_file_name }}.repo"
    codeit_repo_file_basearch: "{{ (ansible_architecture == 'x86_64') | ternary('$basearch', 'SRPMS') }}"
    codeit_repo_file_base_url: "https://repo.codeit.guru/packages/centos/{{ codeit_repo_major_version }}/{{ codeit_repo_file_basearch }}"


The CodeIT repo URL and GPG key URL. Generally, these should not be changed, but if this role is out of date, or if you
need a very specific version, these can both be overridden.

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for
users too:

    - hosts: servers
      roles:
        - memiah.repo_codeit

License
-------

MIT / BSD

Author Information
------------------

This role was created in 2022 by [Memiah Limited](https://github.com/memiah).

