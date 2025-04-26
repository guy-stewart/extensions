# In8 Language Support for VS Code

This extension provides syntax highlighting for the In8 programming language in Visual Studio Code.

## Features

- Syntax highlighting for In8 language constructs
- Recognition of special In8 operators and syntax

## Installation

### Manual Installation

1. Create a folder named `in8-language` in your VS Code extensions directory:
   - Windows: `%USERPROFILE%\.vscode\extensions`
   - macOS/Linux: `~/.vscode/extensions`

2. Copy all the extension files from in8-language into this directory.

3. Add a section for in8-language to the extensions.json file found in the extensions folder, Replace YOUR USER NAME with your own user name:
``` json
    {
        "identifier": {
            "id": "ioMetics.in8",
            "uuid": "198a705e-28bf-4e84-8610-6e2f628dd12d"
        },
        "version": "1.41.0",
        "location": {
            "$mid": 1,
            "path": "/Users/<YOUR USER NAME>/.vscode/extensions/in8-language",
            "scheme": "file"
        },
        "relativeLocation": "in8-language",
        "metadata": {
            "isApplicationScoped": false,
            "isMachineScoped": false,
            "isBuiltin": false,
            "installedTimestamp": 1743091246709,
            "pinned": false,
            "source": "gallery",
            "id": "198a705e-28bf-4e84-8610-6e2f628dd12d",
            "publisherId": "eed56242-9699-4317-8bc7-e9f4b9bdd3ff",
            "publisherDisplayName": "ioMetics",
            "targetPlatform": "darwin-arm64",
            "updated": true,
            "isPreReleaseVersion": false,
            "hasPreReleaseVersion": false,
            "preRelease": false
        }
    },

```
3. Restart VS Code.

## Usage

Files with the `.in8` extension will automatically use this syntax highlighting.

If you need to manually set a file to use In8 highlighting:

1. Open the Command Palette (Ctrl+Shift+P / Cmd+Shift+P)
2. Type "Change Language Mode" and select it
3. Select "in8" from the list

## Syntax Highlighting

This extension provides highlighting for:

- Keywords
- Operators (logical, comparison, arithmetic, prolog-like)
- Strings and characters
- Numbers (integer and float)
- Comments (line and block)
- Predicates
- Method chaining
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