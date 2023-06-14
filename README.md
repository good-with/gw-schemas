# GW Schemas
A collection of both json and yaml schemas used throughout Good With development environments.

## Getting Started
To use these schemas in your development environment, please reference each schema in your preferred IDE's settings.

Below is a step by step tutorial on how to add these schemas to your **VSCode** environment.


1. Make sure the [YAML extension](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml) is installed into your environment
2. Use your *command palette* to navigate your commands (View > Command Palette)
3. Type in *settings* and select *Preferences: Open User Settings (JSON)*
4. Insert the following into your configuration:

```json
"yaml.schemas": {
    "https://raw.githubusercontent.com/good-with/gw-schemas/main/finiq.schema.json": "/*.finiq.yaml",
    "https://raw.githubusercontent.com/good-with/gw-schemas/main/psym.schema.json": "/*.psym.yaml",
    "https://raw.githubusercontent.com/good-with/gw-schemas/main/gwchat.schema.json": "/*.gwchat.yaml",
    "https://raw.githubusercontent.com/good-with/gw-schemas/main/gwbc.schema.json": "/*.gwbc.yaml",
    "https://raw.githubusercontent.com/good-with/gw-schemas/main/dictionary.schema.json": "/dictionary.yaml",
    "https://raw.githubusercontent.com/good-with/gw-schemas/main/broadcasts.schema.json": "/broadcasts.yaml",
},
```

5. Make sure you have the correct schema selected when editing a file (see bottom right of screen - it should NOT say **No JSON Schema)

Read more about schemas here: https://code.visualstudio.com/docs/languages/json