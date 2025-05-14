# SjisValidator

Shft JIS の文字範囲チェックバリデーションを行うためのライブラリ。


## Usage:

Basic usage:

```java
    final String 第一水準漢字 = "亜腕";
    var errors = SjisValidator.validate(第一水準漢字, SjisValidator.VALID_AREA_第一水準漢字);
    // => erros is empty.

    final String 第一水準漢字NG = "╂弌";
    var errors2 = SjisValidator.validate(第一水準漢字NG, SjisValidator.VALID_AREA_第一水準漢字);
    // => erros size is 2.
    //    [
    //        ValidationError[position=0, message=使用できない文字です(╂)],
    //        ValidationError[position=1, message=使用できない文字です(弌)]
    //    ]
```

Other sample, See test code.


## Requirements:

Java 17+


## Install:

### Maven snapshot repository からのインストール

Maven の `settings.xml` に snapshot のリポジトリを追加。

```xml
...(snip)
      <repository>
        <id>snapshot</id>
        <url>https://central.sonatype.com/repository/maven-snapshots</url>
        <releases>
          <enabled>true</enabled>
        </releases>
      </repository>
...(snip)
```

リポジトリを追加したうえで、依存を追加。

```xml
...(snip)
    <dependency>
      <groupId>dev.mikoto2000</groupId>
      <artifactId>sjisvalidator</artifactId>
      <version>1.0-SNAPSHOT</version>
      <scope>compile</scope>
    </dependency>
...(snip)
```



### ソースからビルド・インストール

```sh
git clone https://github.com/mikoto2000/SjisValidator.git
cd SjisValidator
./mvnw install
```

## License:

MIT

## Author:

mikoto2000 <mikoto2000@gmail.com>

