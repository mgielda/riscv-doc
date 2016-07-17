reStructuredText playground
===========================

This document will be used as a testing field for the feasibility of using reST for documenting the RISC-V project,
as a demonstration of features/tips/frameworks and list of useful resources.

Useful resources
----------------

* `Sphinx reST memo <http://rest-sphinx-memo.readthedocs.io/en/latest/ReST.html>`_

Useful features
---------------

This is **not** a comprehensive list of reST features, but rather a selection of what could be useful for documenting an ISA etc.,
with examples.

CSV tables
++++++++++

Easy to generate programmatically, edit with other tools. Well structured and can be very legible if spacing is used correctly.
I advise to use "|" as the delimiter to avoid problems with commas and semicolons. 

.. note::

   CSV tables can be read from external files using the ``:file: path/to/file`` directive. Even more handy for programmatic
   usage.

.. code-block:: reST

   .. csv-table::
      :header-rows: 1
      :delim: |

      a|b|c
      1|2|3

generates:

.. csv-table::
   :header-rows: 1
   :delim: |

   a|b|c
   1|2|3
   
Cons:

* no possibility for cell styling and cells spanning multiple fields
   
Tips & tricks
-------------

Frameworks
----------

* `RTFD <http://readthedocs.org/>`_ (sic, the official abbreviation really is RTFD, see `the project's GitHub <https://github.com/rtfd/readthedocs.org>`_)

TODOs
-----

* reST is heavily missing a JavaScript parser
