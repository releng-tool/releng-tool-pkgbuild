releng-tool pkgbuild
====================

This repository manages a PKGBUILD_ definition used to prepare a releng-tool
release for an Arch Linux system. The ``aur`` directory is synchronized with
this project's AUR package:

 | Arch User Repository - releng-tool
 | https://aur.archlinux.org/packages/releng-tool/

commands
--------

Verify ``PKGBUILD`` is correct:

.. code-block:: shell

   $ namcap PKGBUILD

Build a package using ``makepkg``:

.. code-block:: shell

   $ makepkg

Verify the generated package:

.. code-block:: shell

   $ namcap <built-package-name>

.. _PKGBUILD: https://wiki.archlinux.org/index.php/PKGBUILD
