[![Build Status](https://travis-ci.com/SpokeyWheeler/ids.svg?branch=master)](https://travis-ci.com/SpokeyWheeler/ids)
[![CodeFactor](https://www.codefactor.io/repository/github/spokeywheeler/ids/badge)](https://www.codefactor.io/repository/github/spokeywheeler/ids)

Role Name
=========

ids

Requirements
------------

You need Informix install media and licenses

Role Variables
--------------

Defaults:

*   ids_base_path: Starting point for all product installs - you can install multiple versions
*   ids_install_path: Target path for install
*   ids_tmp_path: Working directory - will be removed
*   ids_version_previously_installed: false

Vars:

*   vendor: hcl or ibm
*   ids_version: version number in full, e.g. 12.10.FC12W1
*   force_ids_install: false or true
*   source_location_of_ids_media: Either a path like "</tmp/installs>" or a URL like "<https://artifactory.example.com/media/hcl/informix/ids/12.10.FC12W1>"

Dependencies
------------

None

Example Playbook
----------------

I expect an inventory group for servers in the inventory file. This isn't really needed for this, but it will be needed when I eventually get around to integrating this into an all-encompassing cluster build.

```yaml
- hosts: servers
  become: true

  roles:
    - { role: ids }
```

License
-------

MIT

Author Information
------------------

<https://github.com/SpokeyWheeler>
