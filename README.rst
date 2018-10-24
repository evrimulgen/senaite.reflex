.. image:: https://raw.githubusercontent.com/senaite/senaite.reflex/master/static/logo.png
   :alt: senaite.reflex
   :height: 64
   :align: center

- **SENAITE.REFLEX**: *Reflex Testing machinery for SENAITE*

.. image:: https://img.shields.io/pypi/v/senaite.reflex.svg?style=flat-square
   :target: https://pypi.python.org/pypi/senaite.reflex

.. image:: https://img.shields.io/github/issues-pr/senaite/senaite.reflex.svg?style=flat-square
   :target: https://github.com/senaite/senaite.reflex/pulls

.. image:: https://img.shields.io/github/issues/senaite/senaite.reflex.svg?style=flat-square
   :target: https://github.com/senaite/senaite.reflex/issues

.. image:: https://img.shields.io/badge/README-GitHub-blue.svg?style=flat-square
   :target: https://github.com/senaite/senaite.reflex#readme


Introduction
============

SENAITE REFLEX adds Reflex Testing capabilities to SENAITE.


Installation
============

Please follow the installations instructions for `Plone 4`_ and
`senaite.lims`_.

To install SENAITE REFLEX, you have to add `senaite.reflex` into the `eggs`
list inside the `[buildout]` section of your `buildout.cfg`::

   [buildout]
   parts =
       instance
   extends =
       http://dist.plone.org/release/4.3.18/versions.cfg
   find-links =
       http://dist.plone.org/release/4.3.18
       http://dist.plone.org/thirdparty
   eggs =
       Plone
       Pillow
       senaite.lims
       senaite.reflex
   zcml =
   eggs-directory = ${buildout:directory}/eggs

   [instance]
   recipe = plone.recipe.zope2instance
   user = admin:admin
   http-address = 0.0.0.0:8080
   eggs =
       ${buildout:eggs}
   zcml =
       ${buildout:zcml}

   [versions]
   setuptools =
   zc.buildout =


**Note**

The above example works for the buildout created by the unified
installer. If you however have a custom buildout you might need to add
the egg to the `eggs` list in the `[instance]` section rather than
adding it in the `[buildout]` section.

Also see this section of the Plone documentation for further details:
https://docs.plone.org/4/en/manage/installing/installing_addons.html

**Important**

For the changes to take effect you need to re-run buildout from your
console::

   bin/buildout


Installation Requirements
-------------------------

The following versions are required for SENAITE REFLEX:

-  Plone 4.3.18
-  senaite.core >= 1.2.9
-  senaite.lims >= 1.2.0


.. _Plone 4: https://docs.plone.org/4/en/manage/installing/index.html
.. _senaite.lims: https://github.com/senaite/senaite.lims#installation
