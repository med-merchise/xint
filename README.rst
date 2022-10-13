Xit Projects (Books)!
=====================

Documentation manager and generator based on 'Sphinx'.

.. note::

   The project is currently in development and is not ready for production
   use.


Install
-------

Development Stage:

  Check `ADR-4 <xit-adr-4_>`__ on base namespace project about how to use
  poetry_ to manage how to evolve projects on development stages.

  **Preliminary Stages:**

     In these stages we will use some dependencies as editable.  For example,
     now::

       xit = {path = "../xit", develop = true}

     will become in the future something like::

       xit = "^0.1.1"

     You need to make sure to clone these repositories in the same parent
     folder used for this one::

       cd ..
       git clone https://github.com/med-merchise/xit.git

.. _xit-adr-4: https://github.com/med-merchise/xit/blob/main/docs/source/adrs/adr-0004-poetry-for-development-stage.rst
.. _poetry: https://python-poetry.org

Production Stage:

  *This section is under construction*

After installation tasks:

  Each of our projects should have a ``backlog-0001`` document with task to
  execute after a project is installed.  This document must be located in the
  ``docs/source/backlog`` directory.


Documentation
-------------

**Note** that because the purpose of this project is to be a documentation
manager, it will be usualy installed in other projects as a development
dependency.

*This section is under construction*
