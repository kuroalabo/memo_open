# readme

# Table of Contents

<!-- @import "[TOC]" {cmd="toc" depthFrom=2 depthTo=6 orderedList=false} -->
<!-- code_chunk_output -->

- [Summary](#summary)
  - [Syntax](#syntax)
  - [Options](#options)
  - [Examples](#examples)
    - [1. `-c`](#1-c)
    - [2. `-f`](#2-f)
    - [3. `-d "," -f`](#3-d-f)
- [Reference](#reference)

<!-- /code_chunk_output -->

## Summary

- cut コマンド。文字列をいい感じに切り取ってくれる
- 範囲指定するとき等に使う`,`や`-`の間にスペースがあるとエラーになるので注意

### Syntax

```shell
$ cut OPTION [FILE]
```

### Options

1. `-c`
    - SYNTAX: `-c RANGE`
    - 文字数ごとに切り取ってくれる
2. `-f`
    - SYNTAX: `-f RANGE`
    - 区切り文字 (Delimiter) ごとに切り取ってくれる
    - デフォルトの区切り文字の値はタブなので注意
3. `-d`
    - SYNTAX `-d "STRING"`
    - 区切り文字 (Delimiter) の指定に使える。基本は `-f` との併用を想定
    - デフォルトの区切り文字の値はタブなので tsv などを cut するときは指定不要

### Examples

#### 1. `-c`

1. Execute
    ```shell
    $ cut -c 1-3
    ```
2. Input (Stdin)
    ```
    Hello
    World
    kurOa
    ```
3. Output (Stdout)
    ```
    Hel
    Wor
    kur
    ```
#### 2. `-f`

1. Execute
    ```shell
    $ cut -f 1,3
    ```
2. Input (Stdin)
    ```
    What    is      your    name?
    ```
3. Output (Stdout)
    ```
    What    your
    ```

#### 3. `-d "," -f`

1. Execute
    ```shell
    $ cut -d "," -f 1,3
    ```
2. Input (Stdin)
    ```
    oihjsih,hjaiohjato,hiajtoijhaoi
    ```
3. Output (Stdout)
    ```
    oihjsih,hiajtoijhaoi
    ```


## Reference

- https://shapeshed.com/unix-cut/
- https://www.geeksforgeeks.org/cut-command-linux-examples/
