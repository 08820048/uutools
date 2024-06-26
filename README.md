
<div align="center">
<img src="https://images.waer.ltd/notes/untools.png" width="140px" />

[中文文档](https://github.com/08820048/uutools/blob/master/REAEME-CN.md)

[![Crates.io](https://img.shields.io/crates/d/untools.svg)](https://crates.io/crates/untools)
[![License](https://img.shields.io/github/license/08820048/untools)](https://github.com/08820048/untools/blob/master/LICENSE)
[![rustc 1.77.0](https://img.shields.io/badge/rust-1.77.0-orange.svg)](https://img.shields.io/badge/rust-1.77.0-orange.svg)
[![Documentation](https://docs.rs/console/badge.svg)](https://docs.rs/untools)
[![GitHub stars](https://img.shields.io/github/stars/08820048/untools)](https://github.com/08820048/untools/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/08820048/untools)](https://github.com/08820048/untools/network/members)
[![GitHub issues](https://img.shields.io/github/issues/08820048/untools)](https://github.com/08820048/untools/issues)
[![Contributors](https://img.shields.io/github/contributors/08820048/untools?style=flat-square)](https://github.com/08820048/untools/graphs/contributors)


A Rust utility crate for converting variable names from `camelCase `to snake_case.
</div>

## Installation


Add the following dependency to your `Cargo.toml` file:

```toml
[dependencies]
untools = "1.0.0" # This is just an example. It is recommended to use the latest version number.
```

## Usage


```rust
use untools::camel_to_snake;

fn main() {
    let camel_case_name = "myVariableName";
    let snake_case_name = camel_to_snake(camel_case_name, true);
    assert!("MY_VARIABLE_NAME', snake_case_name);
}
```

```rust
use untools::batch_convert;

fn main() {
    // Specify the input file, output file, naming convention, and whether to operate in silent mode.
    batch_convert("input.txt", "output.txt", true, false);
}
```

In the example above:

- "`input.txt`" is the path to the input file containing variable names to be converted.
- "`output.txt`" is the path to the output file where the converted variable names will be written.
- true indicates that the variable names will be converted to `SCREAMING_SNAKE_CASE`. Set it to false for `camelCase `conversion.
- false indicates that the program will not run in silent mode.
------------------

## CLI Usage
```shell
$ untools -h
Usage: untools [OPTIONS] <--camel-to-snake|--snake-to-camel|--batch <OUTPUT_FILE>> <INPUT>

Arguments:
  <INPUT>

Options:
  -c, --is-constant
      --camel-to-snake
      --snake-to-camel
      --batch <OUTPUT_FILE>
  -s, --silent
  -h, --help                 Print help
  -V, --version              Print version
$ untools --camel-to-snake "helloWorld" -c -s
HELLO_WORLD
$ untools --snake-to-camel "hello_world" -c -s
HelloWorld
$ untools --camel-to-snake "hello_world" -s
helloWorld
$ untools --batch "input.txt" "output.txt" -s 
```

## Futures

> Here are the features and improvements we plan to add to the tool in the future. If you have any suggestions or ideas, feel free to share!

1. **Support for Multiple Naming Conventions:**
   - Add support for other naming conventions such as `SCREAMING_SNAKE_CASE`.
2. **Batch Conversion Feature:** 
   - :white_check_mark: Allow users to convert multiple variable names at once.
3. **Interactive Mode:**
   - :white_check_mark: Create an interactive command-line interface for a more intuitive user experience. [#3](https://github.com/08820048/untools/pull/3)
4. **File Processing Feature:** 
   - :white_check_mark: Support batch conversion of variable names in files.
5. **Custom Rules:**
   - Enable users to define custom conversion rules.
6. **Integration with Editor Plugins:**
   - Develop editor `plugins `to allow users to use the conversion tool directly in their editors.
7. **GUI Interface:**
   - Develop a graphical user interface for a more user-friendly experience.
8. **Support reverse conversion**
   - :white_check_mark: Convert underscores to `PascalCase `.

If you have any ideas or suggestions regarding the above features, feel free to raise them in the Issues section or directly submit a Pull Request.

----

## License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/08820048/untools/blob/master/LICENSE) file for details.

----

## Star趋势图
[![Stargazers over time](https://starchart.cc/08820048/untools.svg?variant=adaptive)](https://starchart.cc/08820048/untools)
