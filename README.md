dev_packages Cookbook
=====================
This cookbook installs some packages useful for provisioning and development.

This cookbook applies to CentOS 7.

List of packages:

- groupinstall Base
- groupinstall Development Tools
- zlib
- zlib-devel
- curl
- curl-devel
- ImageMagick
- ImageMagick-devel
- gcc
- gcc-c++
- make
- openssl
- openssl-devel
- git
- expect
- pcre
- pcre-devel
- readline-devel
- libxml2
- libxml2-devel
- libxslt
- libxslt-devel
- pam-devel
- nc
- mutt
- htop
- rkhunter
- ncdu

At the end it executes also:
- initialization of rkhunter
- yum update (to update everything on the system)

Requirements
------------
None

Attributes
----------
```json
{
  "dev_packages": {
    "group_install": [
      "..",
      ".."
    ],
    "packages_install": [
      "..",
      ".."
    ]
  }
}
```

#### dev_packages::default
<table>
  <tr>
    <th>Key</th>
    <th>Type</th>
    <th>Description</th>
    <th>Default</th>
  </tr>
  <tr>
    <td><tt>['dev_packages']['group_install']</tt></td>
    <td>Array</td>
    <td>list of 'groups' to be installed</td>
    <td><tt>[See before]</tt></td>
  </tr>
  <tr>
    <td><tt>['dev_packages']['packages_install']</tt></td>
    <td>Array</td>
    <td>list of single packages to be installed</td>
    <td><tt>[See before]</tt></td>
  </tr>
</table>

Usage
-----
#### dev_packages::default
Just include `dev_packages` in your node's `run_list`:

```json
{
  "name":"my_node",
  "run_list": [
    "recipe[dev_packages]"
  ]
}
```
and eventually add more packages (or groups).

Contributing
------------
Need help for testing following best practises, if you can help you are welcome!

License and Authors
-------------------
License: MIT

Authors:

Simone Dall'Angelo

