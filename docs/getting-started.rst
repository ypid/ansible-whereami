Getting started
===============

.. include:: includes/all.rst

.. contents::
   :local:


Example inventory
-----------------

To configure :program:`whereami` on hosts you can put them into the
``ypid_service_whereami`` Ansible inventory group:

.. code:: ini

    [ypid_service_whereami]
    hostname

Example playbook
----------------

Here's an example playbook that uses the ``ypid.whereami`` role:

.. literalinclude:: playbooks/whereami.yml
   :language: yaml

The playbooks is shipped with this role under
:file:`docs/playbooks/whereami.yml` from which you can symlink it to your
playbook directory.
In case you use multiple roles maintained by ypid_, consider
using the `ypid-ansible-common`_.

Ansible tags
------------

You can use Ansible ``--tags`` or ``--skip-tags`` parameters to limit what
tasks are performed during Ansible run. This can be used after host is first
configured to speed up playbook execution, when you are sure that most of the
configuration has not been changed.

Available role tags:

``role::whereami``
  Main role tag, should be used in the playbook to execute all of the role
  tasks as well as role dependencies.

``role::whereami:pkgs``
  Tasks related to system package management like installing or
  removing packages.

``role::whereami:install``
  Tasks related to the installation and patching of :program:`whereami`.

``role::whereami:config``
  Tasks related to the configuration of :program:`whereami`.
