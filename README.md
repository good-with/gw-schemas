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
    "https://raw.githubusercontent.com/good-with/gw-schemas/main/psym.schema.json": "/*.psym.yaml"
},
"json.schemas": [
        {
            "fileMatch": [
                "/*.finiq.json"
            ],
            "url": "https://raw.githubusercontent.com/good-with/gw-schemas/main/finiq.schema.json"
        },
        {
            "fileMatch": [
                "/*.psym.json"
            ],
            "url": "https://raw.githubusercontent.com/good-with/gw-schemas/main/psym.schema.json"
        },
        {
            "fileMatch": [
                "/*.bc.json"
            ],
            "url": "https://raw.githubusercontent.com/good-with/gw-schemas/main/bc.schema.json"
        },
        {
            "fileMatch": [
                "/*.gcf.json"
            ],
            "url": "https://raw.githubusercontent.com/good-with/gw-schemas/main/gcf.schema.json"
        },
    ],
```

5. Make sure you have the correct schema selected when editing a file (see bottom right of screen - it should NOT say **No JSON Schema)

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

2. gcf.json schema
```json
{
    "default": {
        "function": "function-name",
        "description": "",
        "runtime": "nodejs16",
        "entry_point": "myfunction",
        "environment_variables": {
    
        },
        "max_instance_count": 5,
        "min_instance_count": 1,
        "available_memory": "256M",
        "timeout_seconds": 60,
        "max_instance_request_concurrency": 80,
        "available_cpu": "1",
        "event_type": "providers/cloud.firestore/eventTypes/document.create",
        "pubsub_topic": "...",
        "retry_policy": "RETRY_POLICY_RETRY",
        "ingress_settings": "ALLOW_INTERNAL_ONLY"
    },
    "stage": {
        "function": "function-name",
        "description": "",
        "runtime": "nodejs16",
        "entry_point": "myfunction",
        "environment_variables": {
    
        },
        "max_instance_count": 5,
        "min_instance_count": 1,
        "available_memory": "256M",
        "timeout_seconds": 60,
        "max_instance_request_concurrency": 80,
        "available_cpu": "1",
        "event_type": "providers/cloud.firestore/eventTypes/document.create",
        "pubsub_topic": "...",
        "retry_policy": "RETRY_POLICY_RETRY"
    }
}
```
