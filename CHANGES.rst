Changelog
=========

.. include:: includes/all.rst

**ypid.whereami**

This project adheres to `Semantic Versioning <http://semver.org/spec/v2.0.0.html>`__
and `human-readable changelog <http://keepachangelog.com/en/0.3.0/>`__.

The current role maintainer_ is ypid_.


ypid.whereami v0.1.0 - unreleased
---------------------------------

Added
~~~~~

- Initial coding and design. [ypid_]

Changed
~~~~~~~

- Changed namespace from ``whereami_`` to ``whereami__``.
  ``whereami_[^_]`` variables are hereby deprecated and you might need to
  update your inventory. This oneliner might come in handy to do this.

  .. code-block:: shell

     git ls-files -z | xargs --null -I '{}' find '{}' -type f -print0 | xargs --null sed --in-place --regexp-extended 's/\<(whereami)_([^_])/\1__\2/g;'

  [ypid_]
