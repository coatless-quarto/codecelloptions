# codecelloptions: A Quarto Experiment on Options

The `codecelloptions` extension is a Quarto extension designed to improve working with custom code cells and cell options in Quarto.

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/coatless-quarto/codecelloptions)

## Usage

The `codecelloptions` extension does not introduce significant enhancements to your document's content. Instead, it serves as a way for authors to quickly bootstrap their own custom code cell through an extension dependency]().

## Installation

To install the `codecelloptions` extension, follow these steps:

1. Open your terminal.

2. Execute the following command:

```bash
quarto add coatless-quarto/codecelloptions
```

This command will download and install the extension under the `_extensions` subdirectory of your Quarto project. If you are using version control, ensure that you include this directory in your repository.

## Options

The extension allows for extracting options from the hashpipe-styled commands, e.g.

````md
```{custom-python}
#| option1: value1
#| option2: value2

# code here
```
````

You cannot extract options given in `inline` within the code cell engine declaration; nor should you.
