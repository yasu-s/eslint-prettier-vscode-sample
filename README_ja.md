# eslint-prettier-vscode-sample

## 概要

* eslint-plugin-prettier を使用してコードフォーマットを実行するサンプルです。
* Visual Studio Code と ESLint拡張機能を使用することでファイル保存時に自動フォーマットができます。

## 実行環境

* Node.js - 10.x
* Yarn - 1.17.x
* Visual Studio Code - 1.45.x
  * [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) - 2.1.x

## 使用ライブラリ

* eslint - 7.1.x
* prettier - 2.0.x
* eslint-config-prettier - 6.11.x
* eslint-plugin-prettier - 3.1.x

## 動作確認

### 1. サンプルのダウンロード

```bash
git clone git@github.com:yasu-s/eslint-prettier-vscode-sample.git
```

### 2. パッケージインストール  

```bash
cd eslint-prettier-vscode-sample
yarn
```

### 3. サンプルの起動  

```bash
yarn lint:fix
```

### 4. VSCodeの実行結果

![eslint](https://user-images.githubusercontent.com/2668146/70415147-549e3c80-1a9f-11ea-97f7-721d299be225.gif)

## 各種設定

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
