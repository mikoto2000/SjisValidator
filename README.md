# SjisValidator

Shft JIS の文字範囲チェックバリデーションを行うためのライブラリ。


# Usage:

Basic usage:

```java
    final String 全角記号 = "亜腕";
    var errors = SjisValidator.validate(全角記号, SjisValidator.VALID_AREA_第一水準漢字);
    // => erros is empty.

    final String 第一水準漢字NG = "╂弌";
    var errors2 = SjisValidator.validate(第一水準漢字NG, SjisValidator.VALID_AREA_第一水準漢字);
    // => erros size is 2.
```

See test code.


# Requirements:

Java 17+


# Install:

TBD

# License:

MIT

# Author:

mikoto2000 <mikoto2000@gmail.com>

