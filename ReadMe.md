# Word Counter

Word Counter is a Rust crate that can be built as a Python package using the Maturin package. This project is a simple example of how Rust can be used to build a Python package for performance-critical code.

## Prerequisites

To use this package, you will need to have Rust and Maturin installed on your system. You will also need to have a Python environment set up with the necessary dependencies.

## Rust Installation
You can install Rust by following the instructions provided at https://www.rust-lang.org/tools/install. Make sure you have installed a stable version of Rust before proceeding.

## Maturin Installation
You can install Maturin using pip:


```bash 
pip install maturin
```

## Initialization

To start a new Maturin project, you can use the maturin init command. This will generate a basic Rust package with the necessary files for building a Python package. To initialize a new project called word_counter, run the following command:

``` bash
maturin init --bin word_counter
```
This will create a new directory called word_counter with the following files:

- Cargo.toml: The Rust package manifest file.
- src/main.rs: The main Rust file containing the fn main() function.
- src/lib.rs: The Rust library file containing the fn count_words() function.
Development

To make changes to the Rust code and test them in a Python environment, you can use:
```bash
maturin develop 
```
This command will build the Rust code and install the Python package in "editable" mode, so any changes you make to the Rust code will be reflected in the installed package.

## First, activate your Python virtual environment:

```bash
source path/to/your/python/env/bin/activate
```
Then, navigate to the project directory and run the following command:

```bash
maturin develop
```
This will build the Rust code and install the Python package in editable mode. You can now import the word_counter package in a Python script and make changes to the Rust code. The changes will be immediately available in the installed package.

## Build Instructions

Once you have made your changes and are ready to build a release version of the Python package, you can use the following command:

```bash
maturin build
```
This will build a Python package with the name word_counter-[version]-py3-none-any.whl, where [version] is the version number specified in Cargo.toml.

## Usage

You can use the word_counter package just like any other Python package:

```python
from word_counter import count_words

text = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent a ante id libero scelerisque semper."
word_count = count_words(text)

print(word_count)
```

This will output a dictionary with unique words and their occurrences in the text.

License

This project is licensed under the MIT License. See the LICENSE file for details.