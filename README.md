Greengrass AWSCLI
=================

This role provides an installed and configured AWS CLI, ready to call Greengrass
and other AWS APIs.

Build Status
------------

[TBD]

Requirements
------------

You will need to supply AWS credentials to run this role.  


Role Variables
--------------

You will most likely need to set all of the following values.

``` yaml
# The following come from the AWS Console
aws_access_key=<your AWS access key>
aws_secret_key=<your AWS secret key>

```

Dependencies
------------

This role has no particular dependencies.  It has only been tested on
Ubuntu/Debian.

Example Playbook
----------------

Here's an example playbook:

    - hosts: servers
      roles:
         - { role: vmware.awscli }

Getting Started
---------------

For development or testing of this role, follow these steps.

* Clone this repo
* Install ansible and other requirements with pip:
  ```
  pip install -r requirements.txt
  ```
* You can test the role with:
  ```
  molecule converge
  ```

Alternatively, you can build a docker container and test that way.

* Clone this repo
* Build the docker images
  ```
  docker build -t vmware/awscli .
  ```
* Run the image on the target role
  ```
  docker run -it vmware/awscli
  ```

License
-------

Apache 2.0
