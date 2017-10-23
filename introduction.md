# Introduction
The purpose of this document is to define the structure, purpose and api for schema driven UI. The schema is defined as a JSON object and contains the following parts:

## Parts
1. body
1. dataset
1. datasources
1. templates
1. perspectives
1. lookups

### Body
The body property is the main entry point for the schema. A very simple schema may only have a body property to define the view structure.

### Dataset
Dataset defines data structures. When you have a data bound schema you should atleast have one dataset ("model" with id 0).

The basic dataset structure includes:

1. id
1. name
1. fields

The name property is not required but makes the schema more readable.

```json
datasets: [
    {
        "id": 0,
        "name": "model",
        "fields": [
            {
                "name": "id"
            },
            {
                "name": "code"
            },
            {
                "name": "description"
            }
        ]
    }
]
```
