Robot Controller - Ansible
==========================

This project manages configurations for all robot controller devices.

Initial setup
-------------

### robot-controller-01 (K26 SOM)

Set up ubuntu 24.04 based on the image provided [here](https://ubuntu.com/download/amd#kria-k26). On initial boot, configure a password and run

```bash
sudo apt install openssh-server
```

Make sure the device is reachable as `robot-controller-01`, e.g. by adding it to `/etc/hosts`.

Usage
-----

Verify all devices are reachable using

```bash
ansible all -m ping
```

If required, use `-u <user> -k` to specify user and password.

Development
-----------

This project uses [pre-commit](https://pre-commit.com/).
