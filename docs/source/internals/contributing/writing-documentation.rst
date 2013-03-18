=====================
Writing documentation
=====================

There's a helper script for building the docs locally::

    cd docs
    ./test_docs.sh

The actual docs are in ``/docs/source``. This directory structure is a
simplified version of what Django does.

* ``internals/`` contains everything related to Oscar itself, e.g. contributing
  guidelines or design philosophies.
* ``ref/`` is the reference documentation, esp. consisting of
* ``ref/apps/`` which should be a guide to each Oscar core app, explaining it's
  function, the main models, how it relates to the other apps, etc.
* ``topics/`` will contain "meta" articles, explaining how things tie together
  over several apps, or how Oscar can be combined with other solutions.
* ``howto/`` contains tutorial-style descriptions on how to solve a certain
  problem. Ideally, those will be kept to a minimum; as the other docs should
  be understandable enough that necessary steps to achieve a certain goal are
  obvious.
* ``_old/`` contains legacy documents that have not been moved into the new
  structure. Please help get rid of those!

``/index.rst`` is designed as the entry point, and diverges from above
structure to make the documentation more approachable. Other ``index.rst``
files should only be created if there's too many files to list them all.
E.g. ``/index.rst`` directly links to all files in ``topics/`` and
``internals/``, but there's an ``index.rst`` both for the files in ``howto/``
and ``ref/apps/``.
