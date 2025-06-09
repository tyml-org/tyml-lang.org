+++
title = "TYML へようこそ"
description = "マークアップ言語用の型定義言語 TYML の公式サイト"
+++

# 概要
TYMLは任意の設定用言語に対して型をつけることを可能にし、`JsonSchema`を置き換えることを目標としています。
```tyml
// TYMLはこのように記述することができます
/// この記述形式はドキュメントです
/// 値名: 型 の形式で記述します
settings: {
    ip: string
    port: int
    mode: Mode
}

/// enumを定義することも可能です
enum Mode {
    "Debug"
    "Release"
}

/// 構造体として定義することも可能です
type Settings {
    ip: string
    port: int
    mode: Mode
}
```
このTYMLで定義した型を任意の設定用言語で使用することができます。
現在サポートしているのは`ini`と`toml`形式です
```toml
# !tyml ~/test.tyml
# "!tyml"と記述することで型検査が有効になり、
# エディタ支援を受けられるようになります
[settings]
ip = "192.168.1.1"
port = 25565
mode = "Debug"
```

# インストール
実際に利用するには2通りの方法があります

1. VSCodeのマーケットプレイスから`TYML LSP Server for VSCode`をダウンロードする
2. バイナリを利用する