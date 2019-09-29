[![Appveyor Status][]][Appveyor] [![Travis Status][]][Travis] [![CodeDocs Status][]][CodeDocs]

A C library for portable packet creation and injection
======================================================

Libnet is an API to help with the construction and handling of network
packets.  It provides a portable framework for low-level network packet
writing and handling (use libnet in conjunction with libpcap and you can
write some really cool stuff).  Libnet includes packet creation at the
IP layer and at the link layer as well as a host of supplementary and
complementary functionality.

Libnet is very handy with which to write network tools and network test
code.  Some projects, available in Debian/Ubuntu and OpenBSD, using
libnet are:

- [arping](https://github.com/ThomasHabets/arping)
- [ettercap](https://www.ettercap-project.org/)
- [ipguard](http://ipguard.deep.perm.ru/)
- [isic](http://isic.sourceforge.net/)
- [nemesis](https://troglobit.com/projects/nemesis/)
- [packit](http://packetfactory.openwall.net/projects/packit/)
- [tcptraceroute](https://web.archive.org/web/20130424094134/http://michael.toren.net/code/tcptraceroute/)
- [yersinia](https://web.archive.org/web/20180522141004/http://www.yersinia.net/)

See the manpage and sample test code for more detailed information.
Online documentation is available at https://codedocs.xyz/libnet/libnet/

> **NOTE:** Legacy code written for *libnet-1.0.x* WILL NOT WORK with
>           *libnet-1.1.x* or later.  See [MIGRATION](doc/MIGRATION)
>           for porting legacy code.


Building
--------

Libnet employs the [GNU configure and build system][autotools].  The
release tarballs ship with a pre-built `configure` script.  To list
available options, type <kbd>./configure --help</kbd>

When checking out the code from GitHub, use <kbd>./autogen.sh</kbd> to
generate a `configure` script.  For this you need the full suite of the
GNU autotools: autoconf (>=2.69), automake (>=1.14), libtool (>=2.4.2).
On Debian/Ubuntu systems:

    sudo apt install autoconf automake libtool

To build the documentation (optional) you need doxygen and pod2man:

    sudo apt install doxygen pod2man

For neat graphics in the HTML documentation, also install graphviz.
There is also a PDF version of the docs, to build that you need quite a
few more packages:

    sudo apt install texlive-extra-utils texlive-latex-extra \
                     texlive-fonts-recommended latex-xcolor  \
                     texlive-font-utils

Fior Microsoft CHM docs you need the HTML Help Workshop, which is part
of Visual Studio: http://go.microsoft.com/fwlink/p/?linkid=154968, on
UNIX and GNU/Linux systems, see `chmcmd`, which is available in the
[FreePascal](http://www.freepascal.org/) suite:

    sudo apt install fp-utils-3.0.4


Origin & References
-------------------

Libnet is widely used, but had been unmaintained for a long time and its
author unreachable.  This version was forked from the 1.1.3 release
candidate from [packetfactory.net][origin], bug fixed, developed, and
re-released.

Use GitHub issues and pull request feature for questions and patches:

  http://github.com/libnet/libnet

Some old docs are available at:

  http://packetfactory.openwall.net/projects/libnet/index.html

-------------------------------------------------------------------------
- v1.1 (c) 1998 - 2004 Mike D. Schiffman <mike@infonexus.com>  
  http://www.packetfactory.net/libnet
- v1.1.3 and later (c) 2009 - 2013 Sam Roberts <vieuxtech@gmail.com>  
  http://github.com/libnet/libnet
-------------------------------------------------------------------------

[autotools]:       https://autotools.io/
[origin]:          http://packetfactory.openwall.net/projects/libnet/
[Appveyor]:        https://ci.appveyor.com/project/troglobit/libnet
[Appveyor Status]: https://ci.appveyor.com/api/projects/status/fkw05hw8cysfl2p1?svg=true
[Travis]:          https://travis-ci.org/libnet/libnet
[Travis Status]:   https://travis-ci.org/libnet/libnet.png?branch=master
[CodeDocs]:        https://codedocs.xyz/libnet/libnet/
[CodeDocs Status]: https://codedocs.xyz/libnet/libnet.svg
