# PaGe

A Bi-directional template language providing Parser and Generator capabilities.

## Syntax

```
templates ::=
| (macros | environment | <text - {"@", "|]"}>)*

macros ::=
| "@MACRO" namedOrNot "[|" <template> "|]"
| "@SET" namedOrNot "[|" <template> "|]"
| "@USE" namedOrNot "[|" <template> "|]"

environment ::=
| "@REP" separatorOrNot namedOrNot "[|" <template> "|]"
| "@VAL" namedOrNot "[|" <template> "|]"
| "@OPT" namedOrNot "[|" <template> "|]"
| "@OR" namedOrNot ("[|" <template> "|]")+

named ::=
| namedOrNot

separatorOrNot ::=
| ("(" (<text - ")">) ")")?
```

## License

Copyright (C)2014 D. Plaindoux.

This program is free software; you can redistribute it and/or modify it
under the terms of the GNU Lesser General Public License as published
by the Free Software Foundation; either version 2, or (at your option) any
later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Lesser General Public License for more details.

You should have received a copy of the GNU Lesser General Public License
along with this program; see the file COPYING.  If not, write to
the Free Software Foundation, 675 Mass Ave, Cambridge, MA 02139, USA.
