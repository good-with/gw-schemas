# GW Schemas
A collection of both json and yaml schemas used throughout Good With applications.

## Getting Started
To use these schemas in your development environment, please reference each schema in your preferred IDE's settings.

Below is a step by step tutorial on how to add these schemas to your **VSCode** environment.

1. Use your *command palette* to navigate your commands (View > Command Palette)
2. Type in *settings* and select *Preferences: Open User Settings (JSON)*
3. Insert the following into your configuration:

```json
"json.schemas": [
    {
        "fileMatch": [
            "/*.bc.json"
        ],
        "url": "https://raw.githubusercontent.com/good-with/gw-schemas/main/bc.schema.json"
    }
],
```

Read more about schemas here: https://code.visualstudio.com/docs/languages/json

## Examples

1. bc.json schema
```json
{
    {
        "title": "string",
        "message": "string",
        "type": 0,
        "highPriority": false,
        "actionLabel": "string",
        "actionCommand": "https://goodwith.co/"
    }
}
```
