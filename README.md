# coln

A simple bash script which counts the number of columns in the given file.

```shell
$ cat sample.txt 
id      name    height
1       madoka  152
2       homura  155
$ coln sample.txt 
sample.txt      3
```

## Features

- Support all kinds of text format file.
- Support multi-file input.
- Support `\r\n` and `\n` line.
- Allow set `-s skipLine` option to skip top comment lines before real header line.
- Allow set `-t separator` option to customize seperator between columns (default separator is ` `(empty space) or `\t`, you can use `-t ,` for `csv` format file).

## Usage

Just download [coln](coln) file, add executable permission, use `./coln` or `sh coln` to execute, or move it to one of `$PATH` folder for global access.

```shell
chmod a+x coln
./coln [-v] [-s skipLine] [-t seperator] [file ...]
```

## Options

| option | description | example |
| ------ | ----------- | ------- |
| `-v` | enable verbose output while running | / |
| `-s skipLine` | skip top `skipLine` lines before real header line | `coln -s 1 file.txt` |
| `-t separator` | customize seperator between columns | `coln -t , file.csv` |

## TODO

- [x] Support custom header line position
- [x] Support custon header separator
- [ ] Support pipeline input
- [x] Support multi-file <del>or folder</del> input

## Licence

by. bunnyxt, GitHub: [https://github.com/bunnyxt/coln](https://github.com/bunnyxt/coln)

[GNU General Public License v3.0](LICENSE)
