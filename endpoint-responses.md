## Help Endpoint Responses

### /help

```
[
    {
        "command": "validate",
        "url": "/help/validate"
    },
    {
        "command": "parse",
        "url": "/help/parse"
    },
    {
        "command": "generate",
        "url": "/help/generate"
    },
    {
        "command": "convert",
        "url": "/help/convert"
    },
    {
        "command": "bundle",
        "url": "/help/bundle"
    },
    {
        "command": "diff",
        "url": "/help/diff"
    }
]
```
### /help/generate

```
{
    "command": "/generate",
    "method": "POST",
    "summary": "Generate the given AsyncAPI template.",
    "description": "",
    "parameters": [],
    "requestBody": {
        "type": "object",
        "required": [
            "asyncapi",
            "template"
        ],
        "properties": {
            "asyncapi": {
                "description": "AsyncAPI document in JSON or YAML.",
                "oneOf": [
                    {
                        "type": "string"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.0.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.1.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.2.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.3.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.4.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.5.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.6.0.json"
                    }
                ]
            },
            "template": {
                "type": "string",
                "description": "Template name to be generated.",
                "enum": [
                    "@asyncapi/dotnet-nats-template",
                    "@asyncapi/go-watermill-template",
                    "@asyncapi/html-template",
                    "@asyncapi/java-spring-cloud-stream-template",
                    "@asyncapi/java-spring-template",
                    "@asyncapi/java-template",
                    "@asyncapi/markdown-template",
                    "@asyncapi/nodejs-template",
                    "@asyncapi/nodejs-ws-template",
                    "@asyncapi/python-paho-template",
                    "@asyncapi/ts-nats-template"
                ]
            },
            "parameters": {
                "type": "object",
                "description": "Template parameters to be generated. Each template has different parameters that you should check in the documentation, \nwhich is usually located in the template's repository.\nThis field is optional but may be required for some templates.\n",
                "additionalProperties": true
            }
        }
    }
}
```



### /help/validate
```
{
    "command": "/validate",
    "method": "POST",
    "summary": "Validate the given AsyncAPI document.",
    "description": "",
    "parameters": [],
    "requestBody": {
        "type": "object",
        "required": [
            "asyncapi"
        ],
        "properties": {
            "asyncapi": {
                "description": "AsyncAPI document in JSON or YAML.",
                "oneOf": [
                    {
                        "type": "string"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.0.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.1.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.2.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.3.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.4.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.5.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.6.0.json"
                    }
                ]
            }
        }
    }
}
```
### /help/parse
```
{
    "command": "/parse",
    "method": "POST",
    "summary": "Parse the given AsyncAPI document.",
    "description": "",
    "parameters": [],
    "requestBody": {
        "type": "object",
        "required": [
            "asyncapi"
        ],
        "properties": {
            "asyncapi": {
                "description": "AsyncAPI document in JSON or YAML.",
                "oneOf": [
                    {
                        "type": "string"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.0.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.1.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.2.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.3.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.4.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.5.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.6.0.json"
                    }
                ]
            }
        }
    }
}
```
### /help/convert
```
{
    "command": "/convert",
    "method": "POST",
    "summary": "Convert the given AsyncAPI document to the specified version.",
    "description": "",
    "parameters": [],
    "requestBody": {
        "type": "object",
        "required": [
            "asyncapi"
        ],
        "properties": {
            "asyncapi": {
                "description": "AsyncAPI document in JSON or YAML.",
                "oneOf": [
                    {
                        "type": "string"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.0.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.1.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.2.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.3.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.4.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.5.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.6.0.json"
                    }
                ]
            },
            "version": {
                "type": "string",
                "description": "Valid specification versions for the AsyncAPI document.",
                "enum": [
                    "2.0.0",
                    "2.1.0",
                    "2.2.0",
                    "2.3.0",
                    "2.4.0",
                    "2.5.0",
                    "2.6.0",
                    "latest"
                ]
            },
            "language": {
                "type": "string",
                "description": "Language to be converted to.",
                "enum": [
                    "yaml",
                    "yml",
                    "json"
                ]
            }
        }
    }
}
```
### /help/bundle
```
{
    "command": "/bundle",
    "method": "POST",
    "summary": "Bundle the given AsyncAPI document(s).",
    "description": "",
    "parameters": [],
    "requestBody": {
        "type": "object",
        "required": [
            "asyncapis"
        ],
        "properties": {
            "asyncapis": {
                "type": "array",
                "description": "AsyncAPI documents in JSON or YAML.",
                "minItems": 1,
                "items": {
                    "$ref": "#/components/schemas/AsyncAPIDocument"
                }
            },
            "base": {
                "description": "AsyncAPI document in JSON or YAML.",
                "oneOf": [
                    {
                        "type": "string"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.0.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.1.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.2.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.3.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.4.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.5.0.json"
                    },
                    {
                        "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.6.0.json"
                    }
                ]
            }
        }
    }
}
```
### /help/diff
```
{
    "command": "/diff",
    "method": "POST",
    "summary": "Compare the given AsyncAPI documents.",
    "description": "",
    "parameters": [],
    "requestBody": {
        "type": "object",
        "required": [
            "asyncapis"
        ],
        "properties": {
            "asyncapis": {
                "type": "array",
                "minItems": 2,
                "maxItems": 2,
                "items": {
                    "description": "AsyncAPI document in JSON or YAML.",
                    "oneOf": [
                        {
                            "type": "string"
                        },
                        {
                            "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.0.0.json"
                        },
                        {
                            "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.1.0.json"
                        },
                        {
                            "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.2.0.json"
                        },
                        {
                            "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.3.0.json"
                        },
                        {
                            "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.4.0.json"
                        },
                        {
                            "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.5.0.json"
                        },
                        {
                            "$ref": "https://raw.githubusercontent.com/asyncapi/spec-json-schemas/master/schemas/2.6.0.json"
                        }
                    ]
                }
            }
        }
    }
}
```
