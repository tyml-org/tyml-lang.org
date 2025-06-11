+++
title = "QuickStart"
description = "はじめる"
weight = 2
+++

# VSCode上にインストールする
VSCodeを開いて拡張機能のマーケットプレイスから[`TYML for VSCode`](https://marketplace.visualstudio.com/items?itemName=bea4dev.tyml-lsp-vscode)をダウンロードします。

# 型を宣言する
任意のフォルダに以下のような内容でファイル`example.tyml`を作成します。
```tyml
setting: int
```
こうすることで`setting`という名前の設定値が`int`型であることを宣言することができます。

# 型チェックを有効化する
次に、同じフォルダに以下のようなファイル`example.toml`を作成します。
```toml
# !tyml example.tyml
setting = "invalid value"
```
すると型チェックによりエラーが出るはずです。

![tyml_lsp_error_ja](/tyml_lsp_error_ja.png)

最後に以下のように修正します。
```toml
# !tyml example.tyml
setting = 100
```
これでエラーは消えるはずです。