# In8 Language Support for VS Code

This extension provides syntax highlighting for the In8 programming language in Visual Studio Code.

## Features

- Syntax highlighting for In8 language constructs
- Support for In8's Prolog-like features (predicates, facts, queries, rules)
- Recognition of special In8 operators and syntax
- Custom file icons for In8 files

## Installation

### Manual Installation

1. Create a folder named `in8-language` in your VS Code extensions directory:
   - Windows: `%USERPROFILE%\.vscode\extensions`
   - macOS/Linux: `~/.vscode/extensions`

2. Copy all the extension files into this directory.

3. Restart VS Code.

### Building from Source

1. Clone this repository
2. Run `vsce package` to create a `.vsix` file
3. Install the extension using:
   ```
   code --install-extension in8-language-0.0.1.vsix
   ```

## Usage

Files with the `.in8` extension will automatically use this syntax highlighting.

If you need to manually set a file to use In8 highlighting:

1. Open the Command Palette (Ctrl+Shift+P / Cmd+Shift+P)
2. Type "Change Language Mode" and select it
3. Select "In8" from the list

## Syntax Highlighting

This extension provides highlighting for:

- Keywords (`if`, `else`, `while`, `for`, `predicate`, `functor`)
- Operators (logical, comparison, arithmetic, prolog-like)
- Strings and characters
- Numbers (integer and float)
- Comments (line and block)
- Predicates, facts, queries and rules
- Variables (bound, unbound with `?` prefix, and placeholders `_`)

## Customizing Colors

You can customize the colors by adding theme overrides in your settings.json:

```json
"editor.tokenColorCustomizations": {
  "textMateRules": [
    {
      "scope": "keyword.control.in8",
      "settings": {
        "foreground": "#C586C0"
      }
    },
    {
      "scope": "entity.name.function.predicate.in8",
      "settings": {
        "foreground": "#DCDCAA"
      }
    },
    {
      "scope": "variable.unbound.in8",
      "settings": {
        "foreground": "#9CDCFE",
        "fontStyle": "italic"
      }
    }
  ]
}
```

## Extension Settings

This extension doesn't provide any additional settings.

## Using Custom File Icons

To enable the custom In8 file icons:

1. Open the Command Palette (Ctrl+Shift+P / Cmd+Shift+P)
2. Type "File Icon Theme" and select "Preferences: File Icon Theme"
3. Select "In8 Icons" from the list

This will apply the custom In8 file icons to all files with the `.in8` extension in your workspace.

## Known Issues

- This is an initial implementation and may not cover all edge cases
- Some complex syntax patterns might not be highlighted correctly

## Release Notes

### 0.0.1

- Initial release with basic syntax highlighting

## Contributing

If you find any issues or have suggestions for improvements, please submit them to the issue tracker.