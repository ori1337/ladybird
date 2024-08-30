# Helix Configuration
Helix, a modern and efficient text editor, comes with built-in support for clangd (a language server for C/C++) and clang-format (a code formatting tool) out of the box! However, you also need to configure the clangd server to prevent it from improperly inserting headers. To achieve this, create a `.helix/languages.toml` configuration file in your project's root directory. This file allows you to customize language-specific settings, ensuring optimal functionality for C/C++ development within Helix.
```toml
[language-server.ladybird]
command = "clangd"
args = ["--header-insertion=never"]

[[language]]
name = "cpp"
language-servers = ["ladybird"]
```
