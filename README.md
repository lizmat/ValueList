[![Actions Status](https://github.com/lizmat/ValueList/workflows/test/badge.svg)](https://github.com/lizmat/ValueList/actions)

NAME
====

ValueList - Provide an immutable List value type

SYNOPSIS
========

```raku
use ValueList;

my @a is ValueList = ^10;  # initialization follows single-argument semantics
my @b is ValueList = ^10;

set( @a, @b );  # elems == 1
```

DESCRIPTION
===========

The functionality provided by this module will be provided in language level 6.e and higher. If an implementation of ValueList is already available, loading this module becomes a no-op.

Raku provides a semi-immutable Positional datatype: List. A `List` can not have any elements added or removed from it. However, since a list **can** contain containers of which the value can be changed, it is not a value type. So you cannot use Lists in data structures such as `Set`s, because each List is considered to be different from any other List, because they are not value types.

AUTHOR
======

Elizabeth Mattijsen <liz@raku.rocks>

Source can be located at: https://github.com/lizmat/ValueList . Comments and Pull Requests are welcome.

COPYRIGHT AND LICENSE
=====================

Copyright 2022 Elizabeth Mattijsen

This library is free software; you can redistribute it and/or modify it under the Artistic License 2.0.

