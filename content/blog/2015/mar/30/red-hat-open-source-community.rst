Red Hat and the Open Source Community
=====================================

Red Hat has a pretty interesting business model, which is offering support for
software that is a decade old, and which its maintainers want nothing to do
with. This post isn't about whether maintaining old software is a good or a bad
idea. It's about the effect it has on the community.

The Python core developers have ceased providing *any* support for Python 2.6
as of October 2013, but Red Hat will continue to support it in RHEL 5, until
2020. [#]_

Many Python projects (such as Django, Twisted, and PyCA Cryptography) are
therefore looking to drop 2.6 support, to lighten their maintenance burden and
because offering support for an unsupported platform is misleading to users.

This is where we hit an impasse; inevitably users of these projects ask for
some level of support for a version of the library that supports 2.6, because
they are using RHEL which has them pinned on Python 2.6. Red Hat supports their
Python, but not the Python libraries they use.

While Python is a nice language, without the libraries of PyPI it is useless:
no scientific computing, no machine learning, no websites, no access to your
production database, no AWS bindings, no timezone database, no SSH automation,
the list goes on.

Red Hat's business model fundamentally relies on the open source community
offering free labor to support them. Red Hat does not continue to support
Python 2.6 by working with the Python core development team to extend its life
cycle. This means if something like PyCA Cryptography were to support Python
2.6, the entire stack would only be supported for Red Hat's customers, other
individuals who had Python 2.6 would be on an unsupported platform.

This assumption of uncompensated labor to support Red Hat's business is
inequitable. Open Source projects should not feel compelled to support older
versions of software which are only supported commercially. Red Hat itself
needs to consider ways it can continue to offer its support services, without
them becoming burdensome to the open source community. Lastly, Red Hat
customers who wish they could use newer versions of software, should consider
either compiling it themselves, complaining to whoever procured RHEL for them,
or complaining to Red Hat itself, but please don't demand support from already
overburdened volunteers.

.. [#] Technically, RHEL 5 actually comes with Python 2.4, which was last
       updated in 2008. However, Python 2.6 can be installed via EPEL, which
       isn't officially supported by Red Hat, but is usually maintained by
       Fedora developers who work for Red Hat. RHEL 6 officially supports Python
       2.6, and Python 2.7 can be obtained via EPEL for it.
