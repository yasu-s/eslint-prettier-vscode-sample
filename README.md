# eslint-prettier-vscode-sample

## Overview

* This is a sample to execute code format using eslint-plugin-prettier.
* By using Visual Studio Code and ESLint extension, you can format automatically when saving files.

## System requirements

* Node.js - 10.x
* Yarn - 1.17.x
* Visual Studio Code - 1.45.x
  * [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) - 2.1.x

## Used library

* eslint - 7.1.x
* prettier - 2.0.x
* eslint-config-prettier - 6.11.x
* eslint-plugin-prettier - 3.1.x

## Usage

### 1. Download Sample

```bash
git clone git@github.com:yasu-s/eslint-prettier-vscode-sample.git
```

### 2. Installing packages

```bash
cd eslint-prettier-vscode-sample
yarn
```

### 3. Launch sample application

```bash
yarn lint:fix
```

### 4. Execution result of VSCode

![eslint](https://user-images.githubusercontent.com/2668146/70415147-549e3c80-1a9f-11ea-97f7-721d299be225.gif)

## Settings

### .vscode/settings.json

```json
{
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
}
```

### .eslintrc.json

```json
{
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": [
      "error",
      {
        "printWidth": 140,
        "tabWidth": 2,
        "useTabs": false,
        "semi": true,
        "singleQuote": true,
        "trailingComma": "all",
        "bracketSpacing": true,
        "arrowParens": "always"
      }
    ]
  },
  "parserOptions": {
    "sourceType": "module",
    "ecmaVersion": 2015
  }
}
```
