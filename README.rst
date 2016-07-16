RISC-V documentation
====================

A very important aspect of the RISC-V effort will be good documentation of all aspects of the ISA as well surrounding
technologies, topics and ideas.

Tutorials, introductory material and 'user documentation' will also matter, especially as we strive towards more adoption.

Picking the right technology for this end is necessary. The documentation framework has to enable both creating PDF documentation 
(crucial for any technical/datasheet style documentation) as well as HTML - which is necessary for any modern project. Another
important consideration should be the ease of creating the documentation, as we need people to be able to easily describe their
work and collaborate.

LaTeX
-----

LaTeX, while a venerable and traditional standard for all sorts of (especially more 'technically-oriented') documents,
seems ill-suited for adopting as a documentation standard for a new project, as it is quite complex and does not output HTML.

Markdown
--------

Markdown is excellent in terms of adoption and HTML output, but it does not offer proper tooling for LaTeX output.
There is a Markdown-based documentation tool called `MkDocs <http://www.mkdocs.org/>`_, but it only outputs HTML.
Also, many people have complained about Markwdown's inherent inability to represent more complicated document structures due
to the very simplicity that makes it popular.

RST
---

Another option is `ReStructuredText (RST) <https://en.wikipedia.org/wiki/ReStructuredText>`_, a format used extensively in
documetning the Python programming language and its libraries. RST source can be used to generate both HTML and LaTeX/PDF, and in
fact it is designed for technical documentation. The most widely used RST tool is `Sphinx <http://sphinx.pocoo.org/>`_, the
de-facto standard for working with RST documentation, providing convenient extensions, structure, customization options etc.
Sphinx itself is also written in Python, easily extendible and actively developed.

Cons:

- no JavaScript RST parsers for on-the-fly rendering in the browser [#]_

.. [#] I would actually propose that we write one, if we're serious about it
