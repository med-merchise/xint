After installation tasks
========================

Rationale:

  **As a** `programmer`, **I** need to maintain a simple list of tasks , **so
  hat** we can check what to do after adding `xit.books` as a dependency to a
  project.


Full list
---------

- `jupytext` - this tool allows a notebook can use a pair of files, for
  example, ``.md`` and ``.py``.  These two files are synchronized in the
  background when one is modified.  For that reason we disabled globally the
  option ``auto-save`` for Jupyter Notebooks::

    mkdir -p ~/.jupyter/custom
    echo "Jupyter.notebook.set_autosave_interval(0);" \
         >> ~/.jupyter/custom/custom.js

  This is to avoid a warning, see why on the FAQ `"Jupyter warns me that the
  file has changed on disk" <jupyter-warn_>`__.

.. _jupyter-warn: https://jupytext.readthedocs.io/en/latest/faq.html#jupyter-warns-me-that-the-file-has-changed-on-disk

- `voila` - the ``jupyter lab`` preview extension for `Voilà <voila_>`__
  needs to be installed with::

    jupyter labextension install @jupyter-voila/jupyterlab-preview

.. _voila: https://www.kylabendt.com/blog/setting-up-jupyterlab-and-voila/
