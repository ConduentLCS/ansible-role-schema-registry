brandisher.schema-registry
=========
[![Build Status](https://travis-ci.org/brandisher/ansible-role-schema-registry.svg?branch=master)](https://travis-ci.org/brandisher/ansible-role-schema-registry)

Role for installing and configuring Confluent Schema Registry on SLES 12.

Requirements
------------

Presumes that you're installing on SLES 12 with a local repo that has a JDK package.

Role Variables
--------------

* Optional
    * `install_jdk` -- Defaults to "false". jdk\_package is required to be set if `install_jdk` is true
        * `jdk_package` -- A string that should be [jdk package name]=[jdk package version].  The install is done with zypper so anything that zypper can handle syntax wise should work.
    * `install_from_confluent` -- Defaults to "true". Both of the below variables are required if this is "true".  If it's "false", only `schema_registry_rpm_repo` is required.
        * `schema_registry_rpm_repo_key` -- Defaults to "http://packages.confluent.io/rpm/2.0/archive.key".
        * `schema_registry_rpm_repo` -- Defaults to "http://packages.confluent.io/rpm/2.0"
    * `schema_registry_rpm` -- Defaults to "confluent-schema-registry=2.0.1-1"

Dependencies
------------

No dependencies

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: brandisher.schema-registry }

License
-------

BSD-3-Clause

Author Information
------------------

[@brandisher](https://github.com/brandisher)
