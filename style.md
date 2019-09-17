https://barry.warsaw.us/









==============================
GNU Mailman Coding Style Guide
==============================

Copyright (C) 2002-2019 Barry Warsaw


Python coding style guide for GNU Mailman
=========================================

*NOTE*: The canonical version of this style guide can be found at:

http://barry.warsaw.us/software/STYLEGUIDE.txt

This document contains a style guide for Python programming, as used in GNU
Mailman.  `PEP 8`_ is the basis for this style guide so it's recommendations
should be followed except for the differences outlined here.  This document
assumes the use of Python 3.

* Imports are always put at the top of the file, just after any module
  comments and docstrings, and before module globals and constants, but after
  any ``__future__`` imports, or ``__metaclass__`` and ``__all__``
  definitions.

  Imports should be grouped, with the order being:

  1. non-from imports for standard and third party libraries
  2. non-from imports from the application
  3. from-imports from the standard and third party libraries
  4. from-imports from the application

  From-imports should follow non-from imports.  Dotted imports should follow
  non-dotted imports.  Non-dotted imports should be grouped by increasing
  length, while dotted imports should be grouped alphabetically.

  See this flake8 plugin for enforcement of these rules:
  https://gitlab.com/warsaw/flufl.flake8

* In general, there should be one class per module.  Keep files small, but
  it's okay to group related code together.  List everything exported from the
  module in the ``__all__``.

  This library makes this very easy:
  https://pypi.org/project/atpublic/

* Right hanging comments are discouraged, in favor of preceding comments.
  E.g. bad::

    foo = blarzigop(bar)  # if you don't blarzigop it, it'll shlorp

  Good::

    # If you don't blarzigop it, it'll shlorp.
    foo = blarzigop(bar)

  Comments should always be complete sentences, with proper capitalization and
  full stops at the end.

* Put two blank lines between any top level construct or block of code
  (e.g. after import blocks).  Put only one blank line between methods in a
  class.  No blank lines between the class definition and the first method in
  the class.  No blank lines between a class/method and its docstrings.

* Try to minimize the vertical whitespace in a class or function.  If you're
  inclined to separate stanzas of code for readability, consider putting a
  comment in describing what the next stanza's purpose is.  Don't put stupid
  or obvious comments in just to avoid vertical whitespace though.

* Unless internal quote characters would mess things up, the general rule is
  that single quotes should be used for short strings, double quotes for
  triple-quoted multi-line strings and docstrings.  E.g.::

    foo = 'a foo thing'
    warn = "Don't mess things up"
    notice = """Our three chief weapons are:
             - surprise
             - deception
             - an almost fanatical devotion to the pope
             """

* Write docstrings for modules, functions, classes, and methods.  Docstrings
  can be omitted for special methods (e.g. __init__() or __str__()) where the
  meaning is obvious.

* PEP 257 describes good docstrings conventions.  Note that most importantly,
  the """ that ends a multiline docstring should be on a line by itself, e.g.::

    """Return a foobang

    Optional plotz says to frobnicate the bizbaz first.
    """

* For one liner docstrings, keep the closing """ on the same line.

* ``fill-column`` for docstrings should be 78.

* When testing the emptiness of sequences, use ``if len(seq) == 0`` instead of
  relying on the falseness of empty sequences.  However, if a variable can be
  one of several false values, it's okay to just use ``if seq``, though a
  preceding comment is usually in order.

* Always decide whether a class's methods and instance variables should be
  public or non-public.

  Single leading underscores are generally preferred for non-public
  attributes.  Use double leading underscores only in classes designed for
  inheritance to ensure that truly private attributes will never name clash.
  These should be rare.

  Public attributes should have no leading or trailing underscores unless they
  conflict with reserved words, in which case, a single trailing underscore is
  preferable to a leading one, or a corrupted spelling, e.g. ``class_`` rather
  than ``klass``.


.. _`PEP 8`: http://www.python.org/peps/pep-0008.html
.. _`GNU Mailman Python template`: http://bazaar.launchpad.net/~mailman-coders/mailman/3.0/annotate/head%3A/template.py


