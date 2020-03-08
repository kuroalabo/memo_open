# Documentatio

# Table of Contents

<!-- @import "[TOC]" {cmd="toc" depthFrom=2 depthTo=6 orderedList=false} -->
<!-- code_chunk_output -->

- [Summary](#summary)
  - [Examples](#examples)
    - [Input](#input)
    - [Output](#output)
- [Reference](#reference)

<!-- /code_chunk_output -->

## Summary

- github は syntax highlighting に linguist を使用しているのでそれに基づく code line を指定する


### Examples

#### Input


\```shell
ls - al
\```

\```python
s = "Python syntax highlighting"
print s
\```

#### Output

```shell
ls -al
```

```python
s = "Python syntax highlighting"
print s
```


## Reference

- https://help.github.com/en/github/writing-on-github/creating-and-highlighting-code-blocks
    - > We use [Linguist](https://github.com/github/linguist) to perform language detection and to select third-party grammars for syntax highlighting. You can find out which keywords are valid in the [languages YAML file](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml).
- https://github.com/github/linguist/blob/master/lib/linguist/languages.yml
