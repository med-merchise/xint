After installation tasks
========================

Rationale:

  **As a** `programmer`, **I** need to maintain a simple list of tasks , **so
  hat** we can check what to do after adding `xit.books` as a dependency to a
  project.


Full list
---------

- `jupytext` - this tool allows a notebook to use a pair of files to represent
  a single notebook, for example, ``.md`` and ``.py``.  The two files are
  synchronized in the background when one of them is modified.  For that
  reason, to avoid a `warning using notebooks <jupyter-warn_>`__, we disabled
  globally the option ``auto-save`` when ``jupytext`` is used.

  Add to the file ``~/.jupyter/custom/custom.js``.  ::

    $([IPython.events]).on("notebook_loaded.Notebook", function () {
      IPython.notebook.set_autosave_interval(0);
    });

  Also, use a convention in order to include only one of the files to version
  control; ignore the ``.py``.  We use the the following naming convention in
  my ``.gitignore`` file::

    *-notebook.py
    *-nb.py
    *-lab.py
    *-paired.py

.. _jupyter-warn: https://jupytext.readthedocs.io/en/latest/faq.html#jupyter-warns-me-that-the-file-has-changed-on-disk

- `voila` - the ``jupyter lab`` preview extension for `Voilà <voila_>`__
  needs to be installed with::

    jupyter labextension install @jupyter-voila/jupyterlab-preview
