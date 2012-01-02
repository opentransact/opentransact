= OpenTransact a simple secure standard for financial transactions

![OpenTransact Logo](http://www.opentransact.org/images/logo.png)

The goal is to develop a very simple low level standard for transferring an amount of an asset from one account to another.

Most payment systems and existing standards use the messaging paradigm for historical reasons. OpenTransact specifically rejects the message paradigm and prefers the restful resource approach as used on the web with URL's and HTTP at it's core.

We aim to create a new standard from scratch ignoring all legacy systems, while leaving it flexible enough to allow applications built on top of it to deal with legacy systems.

The standard is designed to follow standard RESTful practices and be concise and human readable.

Start at the main site [OpenTransact](http://opentransact.org) for more.

== How to contribute?

Please join the [OpenTransact mailing list](http://groups.google.com/group/opentransact).

Fork the [OpenTransact Standard Project](http://github.com/opentransact/opentransact) and make changes to the file [opentransact.md](https://github.com/opentransact/opentransact/blob/master/opentransact.md) and create a pull request. Please also send a message to the mailing list about your proposed change.

=== Generating xml, html etc files

The [opentransact.md](https://github.com/opentransact/opentransact/blob/master/opentransact.md) file is in  [Markdown](http://daringfireball.net/projects/markdown/syntax) format with RFC2629 extensions from the [Kramdown-rfc2629](https://github.com/cabo/kramdown-rfc2629) tool.

Generally you don't need to understand any of the rfc2629 xml. Just leave it in place and edit the markdown text itself.

We can generate the XML, TXT and HTML files easily so if you don't want to there is no need to install any extra tools.

If you do want to do so you need Ruby on your computer as well as [Gem Bundler](http://gembundler.com/).

Go to the opentransact directory and type:

    bundle

This installs the required ruby gems.

To generate the new files based on your opentransact.md just type:

    rake

=== Contributors License Agreement

If you are planning on making changes to functionality as opposed to just minor text changes, please do sign the [CLA](http://www.opentransact.org/cla.html) to ensure that we can legally use your contributions. Once you've signed it please send a copy to pelle@stakeventures.com




