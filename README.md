# ClamAV

<p align="center">
  <img width="250" height="250" src="https://raw.githubusercontent.com/Cisco-Talos/clamav-devel/dev/0.104/logo.png" alt='Maeve, the ClamAV mascot'>
</p>

<p align="center">
  ClamAV® is an open source antivirus engine for detecting trojans, viruses,
  malware & other malicious threats.
</p>

<p align="center">
  <a href="https://github.com/Cisco-Talos/clamav-devel/actions"><img src="https://github.com/Cisco-Talos/clamav-devel/workflows/CMake%20Build/badge.svg" height="18"></a>
  <a href="https://discord.gg/6vNAqWnVgw"><img src="https://img.shields.io/discord/636023333074370595.svg?logo=discord" height="18"/></a>
  <a href="https://twitter.com/clamav"><img src="https://abs.twimg.com/favicons/twitter.ico" width="18" height="18"></a>
</p>

## Documentation & FAQ

Official documentation can be found online at
[ClamAV.net](https://www.clamav.net/documents).
Our source code release tarballs also includes a copy of the documentation for
[offline](docs/html/UserManual.html) reading.

## ClamAV Signatures

Anyone can learn to read and write ClamAV signatures. Take a look
at the
[signature writing documentation](https://www.clamav.net/documents/creating-signatures-for-clamav)
and
[phishing signature writing documentation](https://www.clamav.net/documents/phishsigs)
to get started!

## Installation Instructions

### Docker

ClamAV can be run using Docker, see [README.Docker.md](README.Docker.md) and
our images on [Docker Hub](https://hub.docker.com/r/clamav/clamav).

#### Build from Source

For comprehensive compile and install instructions, please see
[INSTALL.md](INSTALL.md).

For step-by-step instructions, see our
[online documentation](https://docs.clamav.net/manual/Installing/Installing-from-source-Unix.htmll).

#### Install from a binary package distribution

For binary package distribution installation instructions,
[see the Packages section in our online documentation](https://docs.clamav.net/manual/Installing/Packages.html).

#### Install using an installer (Windows)

We provide installers to install ClamAV on Windows to "C:\\Program Files".
This install method will require you to have Administrator priveleges.

We also provide a "Portable Install Package" (i.e. a zip of the required files)
for users that may wish to run ClamAV without installing it to a system-owned
directory.

For details on how to use either option, head over to the
[Windows Install instructions in the User Manual](https://docs.clamav.net/manual/Installing.html).

### Upgrading from a previous version

Some tips on [how to upgrade](https://docs.clamav.net/faq/faq-upgrade.html)
 from a previous version of ClamAV.

## ClamAV News

For information about the features in this and prior releases, read
[the news](NEWS.md).

Catch up on the latest about ClamAV by reading our
[blog](http://blog.clamav.net) and follow us on Twitter @clamav.

## Join the ClamAV Community

The best way to get in touch with the ClamAV community is to join our
[mailing lists](https://docs.clamav.net/faq/faq-ml.html).

You can also join the community on our
[ClamAV Discord chat server](https://discord.gg/6vNAqWnVgw). If you prefer IRC,
the Discord `#general`, and `#irc-verbose` channels are bridged with the
`#clamav` IRC channel on `irc.freenode.net` using a pair of bots to relay
messages.

## Want to make a contribution?

The ClamAV development team welcomes
[code contributions](https://github.com/Cisco-Talos/clamav-devel),
improvements to
[our documentation](https://github.com/Cisco-Talos/clamav-documentation),
and also [bug reports](https://github.com/Cisco-Talos/clamav-devel/issues).

Thanks for joining us!

## Licensing

ClamAV is licensed for public/open source use under the GNU General Public
License, Version 2 (GPLv2).

See `COPYING.txt` for a copy of the license.

### 3rd Party Code

ClamAV contains a number of components that include code copied in part or in
whole from 3rd party projects and whose code is not owned by Cisco and which
are licensed differently than ClamAV. These include:

- tomsfastmath:  public domain
- Yara: Apache 2.0 license
  - Yara has since switched to the BSD 3-Clause License;
    Our source is out-of-date and needs to be updated.
- 7z / lzma: public domain
- libclamav's NSIS/NulSoft parser includes:
  - zlib: permissive free software license
  - bzip2 / libbzip2: BSD-like license
- OpenBSD's libc/regex: BSD license
- file: BSD license
- str.c: Contains BSD licensed modified-implementations of strtol(), stroul()
  functions, Copyright (c) 1990 The Regents of the University of California.
- pngcheck (png.c): MIT/X11-style license
- getopt.c: MIT license
- Curl: license inspired by MIT/X, but not identical
- libmspack: LGPL license
- UnRAR (libclamunrar): a non-free/restricted open source license
  - Note: The UnRAR license is incompatible with GPLv2 because it contains a
    clause that prohibits reverse engineering a RAR compression algorithm from
    the UnRAR decompression code.
    For this reason, libclamunrar/libclamunrar_iface is not linked at all with
    libclamav. It is instead loaded at run-time. If it fails to load, ClamAV
    will continue running without RAR support.

See the `COPYING` directory for a copy of the 3rd party project licenses.

## Credits

[The ClamAV Team](https://www.clamav.net/about.html#credits)
