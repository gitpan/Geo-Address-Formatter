# perl-Geo-Address-Formatter

Perl CPAN module to take structured address data and format it
according to the various global/country rules.

It is meant to run against a set of configuration and test cases in
<https://github.com/lokku/address-formatting>

The address-formatting repository is added as a [git submodule](http://git-scm.com/book/en/Git-Tools-Submodules). It is
versioned, that means it won't automatically update when you run `git
pull`. To point it to a newer version of the configuration run 

1. `git submodule init`
2. `git submodule update`

This will give you the templates as versions with this repository.
To fetch the latest templates available use
`git submodule foreach git pull origin master`

See also: <http://git-scm.com/book/en/Git-Tools-Submodules>

To submit new countries/territories please see the details in the
[address-formatting repository](https://github.com/lokku/address-formatting), this module just processes the templates

### DEVELOPMENT

    # first install Dist::Zilla
    dzil clean

    # running the test-suite
    dzil test --author

    # don't forget to increase the version number in dist.ini and CHANGES file
    dzil build

    # git push, upload to CPAN
    dzil release


### COPYRIGHT AND LICENCE

Copyright 2014 Lokku Ltd <cpan@lokku.com>

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself, either Perl version 5.10 or,
at your option, any later version of Perl 5 you may have available.

### YOU MAY ALSO ENJOY

This module is in use on the [OpenCage
Geocoder](http://geocoder.opencagedata.com/), converting lat,longs
into nicely formatted strings.
Please give us a try if you have any geocoding needs.