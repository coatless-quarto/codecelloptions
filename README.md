# codecelloptions: A Quarto Experiment on Options

The `codecelloptions` extension is a Quarto extension designed to improve working with custom code cells and cell options in Quarto.

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/coatless-quarto/codecelloptions)

## Usage

The `codecelloptions` extension does not introduce significant enhancements to your document's content. Instead, it serves as a way for authors to quickly bootstrap their own custom code cell through an [extension embedding](https://quarto.org/docs/journals/formats.html#extension-embedding).

## Installation

To install the `codecelloptions` extension inside of your own extension, follow these steps:

1. Open your terminal.

2. Navigate to where your own extension's development location is.

3. Execute the following command:

```sh
quarto add coatless-quarto/codecelloptions --embed <your-extension-name>
```

This command will download and install the extension under the `_extensions` subdirectory of your Quarto extension project. If you are using version control, ensure that you include this directory in your repository.

### File structure

When embedding the extension inside of your own extension, you should see the following folder structure:

```sh
.
└── _extensions
    └── <your-extension-name>
        └── _extensions
            └── coatless-quarto
                └── cellcodeoptions

```

### Registering the extension

Inside of the `_extension.yml`, please include the nested extension under `filters` as the first extension to run: 

```
title: My Extension
author: My Name
version: 0.1.1
quarto-required: ">=1.4.549"
contributes:
  format:
    common:
      filters:
        - coatless-quarto/cellcodeoptions 
        - <your-extension>.lua
```

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
