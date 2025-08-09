# C# Support for Home Assistant VS Code Extension

This extension now includes support for C# development within Home Assistant projects.

## Features Added

### 1. Language Support
- **Language ID**: `home-assistant-csharp`
- **File Extensions**: `.cs`
- **Aliases**: "Home Assistant C#", "C#", "csharp"

### 2. Syntax Highlighting
- Complete C# syntax highlighting using TextMate grammar
- Support for:
  - Keywords (if, else, while, for, class, interface, etc.)
  - Comments (single-line // and multi-line /* */)
  - Strings (regular, verbatim @"", and character literals)
  - Numbers (decimal, hexadecimal, floating-point)
  - Types (built-in and custom)
  - Attributes

### 3. Editor Configuration
- **Tab Size**: 4 spaces (C# standard)
- **Auto Indent**: Advanced indentation rules
- **Format on Save**: Enabled by default
- **Quick Suggestions**: Enabled for better IntelliSense experience

### 4. Code Snippets
The extension includes several useful C# snippets for Home Assistant development:

- `ha_service` - Call a Home Assistant service
- `ha_state` - Get entity state from Home Assistant
- `ha_event` - Listen for Home Assistant events
- `ha_websocket` - Connect to Home Assistant WebSocket API
- `ha_automation` - Create a Home Assistant automation class
- `ha_component` - Create a custom Home Assistant component
- `ha_device` - Create a Home Assistant device class

### 5. Language Configuration
- **Comments**: Support for both line comments (`//`) and block comments (`/* */`)
- **Brackets**: Auto-closing and matching for `{}`, `[]`, `()`, `<>`
- **String Quotes**: Auto-closing for `"` and `'`
- **Folding**: Support for #region/#endregion folding markers
- **Word Pattern**: Optimized for C# identifiers

## Files Added/Modified

### New Files
1. `syntaxes/csharp-language-configuration.json` - C# language configuration
2. `syntaxes/external/csharp.tmLanguage.json` - C# TextMate grammar
3. `src/snippets/homeassistant_csharp.json` - C# snippets for Home Assistant

### Modified Files
1. `package.json` - Added C# language definition, grammar, snippets, and configuration
2. `src/extension.ts` - Added C# document selector and language configuration

## Usage

1. Open any `.cs` file in a Home Assistant workspace
2. The extension will automatically activate and provide C# language support
3. Use the provided snippets by typing the prefix (e.g., `ha_service`) and pressing Tab
4. Enjoy syntax highlighting and proper indentation for C# code

## Example Usage

Here's a simple example of using the snippets to create a Home Assistant service call:

```csharp
// Type 'ha_service' and press Tab to expand this snippet
await hass.CallServiceAsync("light", "turn_on", new {
    entity_id = "light.living_room",
    brightness = 255
});
```

## Integration with Home Assistant

This C# support is designed to work with Home Assistant C# libraries and frameworks such as:
- NetDaemon
- HassClient
- Custom Home Assistant integrations written in C#

The snippets and configuration are optimized for these common use cases while maintaining compatibility with general C# development.

## Requirements

- VS Code 1.100.0 or higher
- This extension activated in a Home Assistant workspace
- Optional: C# Dev Kit extension for advanced IntelliSense and debugging capabilities

## Notes

- The C# language support is automatically activated when opening `.cs` files in a Home Assistant workspace
- All standard VS Code C# features work alongside this extension's enhancements
- The syntax highlighting and language features are optimized for Home Assistant development patterns
