GitEnv
======

Ansible role for installing `GitEnv <https://github.com/ruslo/gitenv>`__
and configs.

WARNING: This script is **destructive** and overwrite some
`dot-config <https://github.com/ruslo/configs/blob/92d879131cc0879766b35c85140dbd9d531fd29a/setup.py#L140-L151>`__
files!

Role Variables
--------------

================== ============================== =================
Name               Description                    Default
================== ============================== =================
gitenv_working_dir Directory to clone 'gitenv' to $HOME/work/gitenv
gitenv_check_zsh   Check that SHELL is ZSH        true
================== ============================== =================

Example Playbook
----------------

Clone this repository:

.. code-block:: none

  > git clone https://github.com/ansible-stuff/gitenv
  > cd gitenv
  [gitenv]>

Copy inventory sample from ``sample/hosts`` and fill it with information about
your remote:

.. code-block:: none

  [gitenv]> cp sample/hosts hosts
  [gitenv]> vim hosts

Run playbook:

.. code-block:: none

  [gitenv]> ansible-playbook --inventory-file hosts gitenv.yml --ask-become-pass

License
-------

`BSD <https://github.com/ansible-stuff/gitenv/blob/master/LICENSE>`__

Author Information
------------------

Ruslan Baratov <ruslan_baratov@yahoo.com>