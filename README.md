# codecelloptions: A Quarto Experiment on Options

The `codecelloptions` extension is a standalone experiment for extracting code cell options.

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/coatless-quarto/codecelloptions)

## Usage

The `codecelloptions` extension does not introduce significant enhancements to your document's content. Instead, it serves as a peek behind the scenes at establishing a parser in Lua for extracting code cell options.

## Installation

To install the `codecelloptions` extension, follow these steps:

1. Open your terminal.

2. Execute the following command:

```bash
quarto add coatless-quarto/codecelloptions
```

This command will download and install the extension under the `_extensions` subdirectory of your Quarto project. If you are using version control, ensure that you include this directory in your repository.

## Options

### Inline

````md
```{custom-python, option1=value1, option2=value2}
# python code here
```
````

### Hashpipe

````md
```{custom-python}
#| option1: value1
#| option2: value2

# python code here
```
````

# Conclusion

TBD
