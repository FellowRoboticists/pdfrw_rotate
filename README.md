pdfrw_rotate
============

A tool to rotate all the pages of a PDF by a modulus of 90 degrees.

This command-line executable is a modification of the 'rotate.py'
example provided with the 'pdfrw' library.

Usage
-----

    $ pdfrw_rotate.py <input-pdf> <rotation> <output-pdf>

Where:

* input-pdf: the PDF document whose pages are to be rotated
* rotation: the angle to be rotated. Must be 90, 180 or 270
* output-pdf: the PDF to be created with the rotated pages

Building/Packaging
------------------

As usual with stuff like this, you should change the revision number
before publishing the package. This is located in setup.py.

To prepare the distribution for publishing:

    $ python setup.py sdist

This will place the versioned tar ball into the dist directory.

Use twine to publish the package:

    $ twine upload dist/<tarball-name>

If you want to install the package, just

    $ pip install pdfrw_rotate

I'm no expert at packaging, so use this (https://packaging.python.org/tutorials/distributing-packages/#description) 
to figure out other packaging options (like using the test.pypi.org site to test
your packaging).
