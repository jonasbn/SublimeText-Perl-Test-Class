SublimeText-Perl-Test-Class
===========================

This package provides snippets for Perl's [Test::Class](https://metacpan.org/pod/Test::Class) for [Sublime Text 2](http://www.sublimetext.com/2)

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

This package can with luck be used with the [package](https://github.com/jonasbn/SublimeText-Perl-Test-More) for Perl's Test::More for Sublime Text 2.

# Installation

1. [Download](https://github.com/jonasbn/SublimeText-Perl-Test-Class/archive/master.zip) the zip file
2. Unpack it in your Sublime Text directory
3. Start using it! (see section above)

# Issues

Please report any issues via [github](https://github.com/jonasbn/SublimeText-Perl-Test-Class/issues).

# Motivation

Organizing your tests using Test::Class is really useful and since Test::Class can be used across projects/distributions this package can assist in speeding up your development. 

# License

The package is licensed under the Artistic License 2.0 and pull-requests are most welcome.

jonasbn, Copenhagen/Denmark