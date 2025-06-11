+++
title = "Welcome to TYML"
description = "Official site for the type definition language TYML for markup languages"
+++

# Overview
TYML makes it possible to add types to any configuration language and aims to replace `JsonSchema`.

```tyml
// TYML can be written like this
/// This style of comment is documentation
/// Write in the form valueName: Type
settings: {
    ip: string
    port: int
    mode: Mode
}

/// You can also define enums
enum Mode {
    "Debug"
    "Release"
}

/// You can also define a struct
type Settings {
    ip: string
    port: int
    mode: Mode
}
````

The types defined in TYML can be used with any configuration language.
Currently supported formats are `ini` and `toml`.

```toml
# !tyml ~/test.tyml
# By writing “!tyml” type checking is enabled
# and you can benefit from editor assistance.
# You can also specify a URL directly.
[settings]
ip = "192.168.1.1"
port = 25565
mode = "Debug"
```

# Intuitive Error Messages

When you validate configuration values, TYML strives to produce clear, intuitive messages.

![tyml_error_en](/tyml_error_en.png)

# Installation

There are two ways to start using TYML:

1. Download **[`TYML for VSCode (QuickStart)`](/quick-en)** from the VS Code Marketplace
2. Use a **[prebuilt binary](https://github.com/tyml-org/tyml/releases)** (or run `cargo install`)