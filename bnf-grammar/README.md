# BNF Grammar Extension for VS Code

This extension provides syntax highlighting for BNF (Backus-Naur Form) grammar files in Visual Studio Code.

## Features

- Syntax highlighting for BNF notation
- Support for .bnf and .grammar file extensions
- Bracket matching and auto-closing pairs
- Comment toggling with `;` for line comments and `/* */` for block comments

## Example

The extension will highlight BNF grammar files like this:

```bnf
<syntax>     ::= <rule> | <rule> <syntax>
<rule>       ::= <opt-whitespace> "<" <rule-name> ">" <opt-whitespace> "::=" <opt-whitespace> <expression> <line-end>
<expression> ::= <term> | <term> <opt-whitespace> "|" <opt-whitespace> <expression>
<term>       ::= <literal> | "<" <rule-name> ">"
<literal>    ::= '"' <text> '"' | "'" <text> "'"
```

## Installation

### From VS Code Marketplace

1. Open VS Code
2. Go to Extensions (Ctrl+Shift+X)
3. Search for "BNF Grammar"
4. Click Install

### From VSIX File

1. Download the .vsix file
2. Open VS Code
3. Go to Extensions (Ctrl+Shift+X)
4. Click on the "..." (More Actions) button at the top of the Extensions panel
5. Select "Install from VSIX..."
6. Navigate to and select the downloaded .vsix file

### Manual Installation

1. Copy the extension files to your VS Code extensions folder:
   - Windows: `%USERPROFILE%\.vscode\extensions\bnf-grammar`
   - macOS/Linux: `~/.vscode/extensions/bnf-grammar`

## Building the Extension

If you want to build the extension yourself:

1. Clone this repository
2. Make sure you have Node.js installed
3. Install vsce: `npm install -g @vscode/vsce`
4. Run `vsce package` in the extension directory
5. This will create a .vsix file that you can install in VS Code

## License

This extension is licensed under the MIT License.