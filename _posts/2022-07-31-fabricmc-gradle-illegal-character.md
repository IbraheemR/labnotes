---
title: "FabricMC/Gradle: Illegal character ((CTRL-CHAR, code 31))"
---

## Context:

- Creating a new fabric mod from fabricmc/fabric-example-mod
- Using IDEA community edition on Ubuntu 22.04 LTS

Note: this was typed in a hurry, might be slightly inaccurate (I'm a java noob)

## Symtoms:

An error message like the followning, which would happen for any gradle task.

Additionally, could not even run `gradle clean`, which usually fixes weird errors.

```

```
Illegal character ((CTRL-CHAR, code 31)): only regular white space (\r, \n, \t) is allowed between tokens
 at [Source: UNKNOWN; line: 1, column: 2]


Caused by: com.fasterxml.jackson.core.JsonParseException: Illegal character ((CTRL-CHAR, code 31)): only regular white space (\r, \n, \t) is allowed between tokens
 at [Source: (String)"\u001F?\u0008\u0000h??b\u0000\u0003???e?%?+\u0010?pEf>\u001DLm?u/?hiB????.4Q\u0000\u0004?.\u0008???N?{_xD$???#?@%*2?\u0001;q????\u007F??O??????????\u007F?\u007F??????=???g???????????_??/\u007F??w?_????\u007F??\u007F??/????\u007F???????????^?3_?\u0017??????d??o\u007F??_\u007F??x??????/\u007F???????????Q???\u007F?\u007F???\u007F???????_\u001EuR_?;?.2Dr????%#?$?Il)??????\u007F???_?????\u0009?~??\u0013?? ~\u0009?\u000B??\u0015?\u000B???\u0013?\u001F~???\u000FP??|a?????[E?!/ ???\u001F?\u007F?c?s?????i\u007FtT?~d?u???7??%???5v\u0019\u0003??2{?qN\u0018?c??#????????A)?????\u0007T??\u0017?\u007F??\u000B?\u0013??9??j?r?\\u0007?pX9,^?a???B?i \u007F???P?\u007F?h?L??)?rS???x?3?3?Y\u0016A?x\u0014`??\u00000y??\u0016?\u0016X??N?C\u001A?=\u000B?\u000B????E?\u0019??\u001Ci ?rl???`f???f?c?\u0009?\u0003?Y\u0006??\u001Dir?4\u0014?}??/"[truncated 28504 chars]; line: 1, column: 2]
```

## Working Solution:

Delete the gradle directory in user home

- `rm -rf ~/.gradle`

## Questions/search terms that didn't help:

- The whole or parts of the error message

## Questions/search terms that did help:

Searched for the error message in the [fabric discord server](https://fabricmc.net/discuss/)
 
Others seem to have been encountering this recently as well.