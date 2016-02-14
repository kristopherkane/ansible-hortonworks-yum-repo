Local Hortonworks Software Repository Management
=========

Management of local yum HTTP repositories for the Hortonworks Data Platform

Requirements
------------

None

Role Variables
--------------

The three booleans determine if that repository should be updated. 

```
ambari_base_version: "2.x"
ambari_el_version: "6"
ambari_version: "2.2.0.0"
ambari_base_url: "http://public-repo-1.hortonworks.com/ambari/centos{{ ambari_el_version }}/{{ ambari_base_version }}/updates/{{ ambari_version }}"
ambari_repo_file: "{{ ambari_base_url }}/ambari.repo"
ambari_repo_id: "Updates-ambari-{{ ambari_version }}"
ambari_repo_install_directory: "/var/www/html/repos"
update_ambari: "true"

hdp_base_version: "2.x"
hdp_el_version: "6"
hdp_version: "2.3.4.0"
hdp_base_url: "http://public-repo-1.hortonworks.com/HDP/centos{{ hdp_el_version }}/{{ hdp_base_version }}/updates/{{ hdp_version }}"
hdp_repo_file: "{{ hdp_base_url }}/hdp.repo"
hdp_repo_id: "HDP-{{ hdp_version }}"
hdp_repo_install_directory: "/var/www/html/repos"
update_hdp: "true"

utils_el_version: "6"
utils_version: "1.1.0.20"
utils_base_url: "http://public-repo-1.hortonworks.com/HDP-UTILS-{{ utils_version }}/repos/centos{{ utils_el_version }}"
utils_repo_file: "{{utils_base_url}}/hdp-util.repo"
utils_repo_id: "HDP-UTILS-{{ utils_version }}"
utils_repo_install_directory: "/var/www/html/repos"
update_utils: "true"
```

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
