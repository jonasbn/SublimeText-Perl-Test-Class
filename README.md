SublimeText-Perl-Test-Class
===========================

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

This package provides snippets for Perl's [Test::Class](https://metacpan.org/pod/Test::Class) for [Sublime Text 2 and 3](http://www.sublimetext.com/)

<!-- MarkdownTOC depth=1 -->

- [Introduction](#introduction)
- [Installation](#installation)
- [Issues](#issues)
- [Motivation](#motivation)
- [History](#history)
- [License](#license)

<!-- /MarkdownTOC -->

<a name="introduction"></a>
# Introduction

The package is currently offering the following snippets:

```perl
testclass
testmethod
```

`testclass` is a variation of the snippet from the builtin Perl package: `package`. It unfolds boilerplate code for a test class (Test::Class) holding the following body of code:

```perl
package Test::Class::ClassName;

use strict;
use warnings;
use base qw(Test::Class);
use Test::More;

#run prior and once per suite
sub startup : Test(startup) {
    # body...

    return 1;
}

#run after and once per suite
sub shutdown : Test(shutdown) {
    # body...

    return 1;
}

#run prior and once per test method
sub setup : Test(setup) {
    # body...

    return 1;
}

#run after and once per test method
sub teardown : Test(teardown) {
    # body...

    return 1;
}

1;
```

`testmethod` is a variation of the snippet from the builtin Perl package: `sub`. It unfolds a more specialized variation of a subroutine.

```perl
sub testmethod_name : Test(number_of_tests) {
    my ($self) = @_;
    # body...

    return return_value;
}
```

This package can with luck be used with the [package](https://github.com/jonasbn/SublimeText-Perl-Test-More) for Perl's [Test::Class](https://metacpan.org/pod/Test::Class) for **Sublime Text 2 and 3**.

<a name="installation"></a>
# Installation

For installation several options are available.

<a name="via-package-control"></a>
## Via [Package Control](https://packagecontrol.io/):

- `Control`+`Shift`+`P` on Linux/Windows,
- `Command`+`Shift`+`P` on OS X,
- or for any OS
  1. Select `Tools->Command Palette` from the menu
  2. Select `Package Control: Install Package`
  3. Select **perl-Test-Class** from the list of available packages

<a name="git"></a>
## Git:

Clone the repository in your Sublime Text Packages directory.

`$ git clone https://github.com/jonasbn/perl-Sublime-Test-Class`

The advantage of using either Package Control or git is, that the plugin will be automatically updated.

See also the [Package Control page](https://packagecontrol.io/packages/perl-Test-Class) for this plugin. 

<a name="from-zip"></a>
## From ZIP

### Sublime Text 3

1. [Download](https://github.com/jonasbn/SublimeText-Perl-Test-Class/archive/master.zip) the zip file
2. Unpack it in your Sublime Text directory, as per OS and Sublime Text 
  - OS X    ~/Library/Application Support/Sublime Text 3/Packages/
  - Linux   ~/.config/sublime-text-3/Packages/
  - Windows %APPDATA%\Sublime Text 3\Packages\
3. Start using it! (see section above)

### Sublime Text 2

1. [Download](https://github.com/jonasbn/SublimeText-Perl-Test-Class/archive/master.zip) the zip file
2. Unpack it in your Sublime Text directory, as per OS and Sublime Text 
  - OS X    ~/Library/Application Support/Sublime Text 2/Packages/
  - Linux   ~/.config/sublime-text-2/Packages/
  - Windows %APPDATA%\Sublime Text 2\Packages\
3. Start using it! (see section above)

<a name="issues"></a>
# Issues

Please report any issues via [github](https://github.com/jonasbn/SublimeText-Perl-Test-Class/issues).

<a name="motivation"></a>
# Motivation

Organizing your tests using Test::Class is really useful and since [Test::Class](https://metacpan.org/pod/Test::Class) can be used across projects/distributions this package can assist in speeding up your development. 

<a name="history"></a>
# History

<a name="2015-08-15-100"></a>
## 2015-08-15 1.0.0

- Initial version

<a name="license"></a>
# License

The package is licensed under the Artistic License 2.0 and pull-requests are most welcome, please see [the contribution guidelines](CONTRIBUTING.md).

jonasbn, Copenhagen/Denmark
