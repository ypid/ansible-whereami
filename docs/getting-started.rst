Getting started
===============

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

Here's an example playbook that can be used to manage whereami::

    ---
    - name: Configure whereami
      hosts: 'ypid_service_whereami'
      become: True

      roles:

        - role: ypid.whereami
          tags: [ 'role::whereami' ]

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

``role::whereami:install``
  Tasks related to the installation of :program:`whereami`.

``role::whereami:config``
  Tasks related to the configuration  of :program:`whereami`.
