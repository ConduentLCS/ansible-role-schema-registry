brandisher.schema-registry
=========
[![Build Status](https://travis-ci.org/brandisher/ansible-role-schema-registry.svg?branch=master)](https://travis-ci.org/brandisher/ansible-role-schema-registry)

Role for installing and configuring Confluent Schema Registry on SLES 12.

Requirements
------------

Presumes that you're installing on SLES 12 with a local repo that has a JDK package.

Role Variables
--------------

* Required
    * jdk\_package -- A string that should be [jdk package name]=[jdk package version].  The install is done with zypper so anything that zypper can handle syntax wise should work.
* Optional
    * schema\_registry\_rpm\_repo\_key -- Defaults to "http://packages.confluent.io/rpm/2.0/archive.key".
    * schema\_registry\_rpm\_repo -- Defaults to "http://packages.confluent.io/rpm/2.0"
    * schema\_registry\_rpm -- Defaults to "confluent-schema-registry=2.0.1-1"

Dependencies
------------

No dependencies

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: brandisher.schema-registry, jdk_package: "jdk=1.8.0_u71" }

License
-------

BSD-3-Clause

Author Information
------------------

[@brandisher](https://github.com/brandisher)
