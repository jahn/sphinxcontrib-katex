Contributing
------------

If you find errors, omissions, inconsistencies or other things that need
improvement, please create an issue or a pull request at
http://github.com/hagenw/sphinxcontrib-katex/.
Contributions are always welcome!

Instead of pip-installing the latest release from PyPI, you should get the
newest development version from Github_::

   git clone https://github.com/hagenw/sphinxcontrib-katex.git
   cd sphinxcontrib-katex
   python setup.py develop --user

.. _Github: http://github.com/hagenw/sphinxcontrib-katex/

This way, your installation always stays up-to-date, even if you pull new
changes from the Github repository.

If you prefer, you can also replace the last command with::

   pip install --user -e .

... where ``-e`` stands for ``--editable``.


New releases are made using the following steps:

#. Bump version number in ``sphinxcontrib/katex.py``
#. Update ``NEWS.rst``
#. Commit those changes as "Release x.y.z"
#. Create an (annotated) tag with ``git tag -a x.y.z``
#. Clear the ``dist/`` directory
#. Create a source distribution with ``python3 setup.py sdist``
#. Create a wheel distribution with ``python3 setup.py bdist_wheel --universal``
#. Check that both files have the correct content
#. Upload them to PyPI with twine_: ``twine upload dist/*``
#. Push the commit and the tag to Github and `add release notes`_ containing a
   link to PyPI and the bullet points from ``NEWS.rst``

.. _twine: https://pypi.python.org/pypi/twine
.. _add release notes: https://github.com/hagenw/sphinxcontrib-katex/tags
