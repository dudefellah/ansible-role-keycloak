dudefellah.keycloak
=========

Install and prepare a Keycloak install using the
"[OpenJDK](https://www.keycloak.org/getting-started/getting-started-zip)"
method.

Requirements
------------

The config file lists are merged using
[community.general.lists_mergeby](https://docs.ansible.com/ansible/devel/collections/community/general/lists_mergeby_filter.html),
so that collection will need to be present for this role to work.

Role Variables
--------------

All role variables are listed and annotated in
[defaults/main.yml](defaults/main.yml).  Please see that file for up-to-date
details on the available variables.

Dependencies
------------

As mentioned in the `Requirements` section, this role uses a module from
the `community.general` collection, so you'll need to ensure that it's
installed on your controller.  The current version as of this writing is
`5.8.0`, so this or future versions should be pretty safe.  You can probably
make use of older collections too, but I don't know when the `lists_mergeby`
module was originally added to that collection, so I'm too lazy to find a
minimum version.

Example Playbook
----------------

    - hosts: keycloak
      roles:
         - role: dudefellah.keycloak
           keycloak_db_username: keycloak
           keycloak_db_password: abc123
           # ... etc

License
-------

GPLv2+

Author Information
------------------

Dan - github.com/dudefellah
