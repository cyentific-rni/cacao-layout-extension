# CACAO Coordinates Specification Version 1.0

This repo defines the CACAO Canvas and Coordinates extension definitions and validation schemas for the purpose of visually representing CACAO playbooks as accurate and consistent to the extent possible across implementations.

This specification defines the Canvas and Coordinates schemas for CACAO Security Playbooks aimed to be used synergistically for the purpose of visually/graphically representing CACAO playbooks to the extent possible in a consistent, repeatable, and accurate manner. The CACAO specification permits extending the playbooks schema via extension definitions that provide detailed information about the extensions that are in use in a playbook.

The full CACAO Coordinates specification is available here: [CACAO-Coordinates-Schema-v1.0](https://docs.oasis-open.org/cacao/coordinates/v1.0/coordinates-v1.0.html)

## Extension Definitions

This specification defines two associated extensions.
One  in section 4 for defining a Canvas size which extends the CACAO Playbook Properties (section 3.1 in CACAO specification [CACAO-Security-Playbooks-v2.0](https://docs.oasis-open.org/cacao/security-playbooks/v2.0/security-playbooks-v2.0.html)) and one in section 7 for Coordinates which can be used with Workflow Steps and Agents and Targets to layout the said constructs graphically.

The two associated Extension Definitions are identified by the following unique identifiers and are presented in sections 4 and 7, respectively.:

- **Canvas Extension Definition:** `extension-definition--d03cf830-2e1a-49b4-a5ee-4bfa704f506a`
- **Coordinates Extension Definition:** `extension-definition--418ee24c-9cb1-46d9-afa5-309e01aabc7f`

### Canvas Extension Definition

Canvas Extension Definition: `extension-definition--d03cf830-2e1a-49b4-a5ee-4bfa704f506a`

```JSON
{
   "type": "extension-definition",
   "name": "CACAO canvas",
   "description": "Extension definition for the Canvas size in which a CACAO playbook is graphically represented/visualized.",
   "created_by":"identity--5abe695c-7bd5-4c31-8824-2528696cdbf1",
   "schema": "placeholder for JSON Schema in CACAO TC Github Repo",
   "version": "1.0.0",
   "external_references": [
     {
       "name": "CACAO Coordinates Specification.",
       "description": "Specification for CACAO Playbooks Canvas and Coordinates extensions.",
       "source": "[CACAO-Coordinates-Schema-v1.0] CACAO Coordinates Schema Version 1.0. Edited by Vasileios Mavroeidis and Mateusz Zych. 07 November 2023. OASIS Committee Specification Draft 01. https://docs.oasis-open.org/cacao/coordinates/v1.0/csd01/coordinates-v1.0-csd01.html. Latest version: https://docs.oasis-open.org/cacao/coordinates/v1.0/coordinates-v1.0.html.",
       "url": "https://docs.google.com/document/d/1eWRxX3kKELOU_08ee013vDRrWYRu9JqS2LIt4Nk-F10/edit"
     }
   ]
 }
```

### Coordinate Extension Definition

Coordinates Extension Definition: `extension-definition--418ee24c-9cb1-46d9-afa5-309e01aabc7f`

```JSON
{
   "type": "extension-definition",
   "name": "CACAO coordinates",
   "description": "Extension definition for Coordinates allowing CACAO Playbooks to be graphically represented on a canvas.",
   "created_by":"identity--5abe695c-7bd5-4c31-8824-2528696cdbf1",
   "schema": "placeholder for JSON Schema in CACAO TC Github Repo",
   "version":"1.0.0",
   "external_references": [
     {
       "name": "CACAO Coordinates Specification.",
       "description": "Specification for CACAO Playbooks Canvas and Coordinates.",
       "source": "[CACAO-Coordinates-Schema-v1.0] CACAO Coordinates Schema Version 1.0. Edited by Vasileios Mavroeidis and Mateusz Zych. 07 November 2023. OASIS Committee Specification Draft 01. https://docs.oasis-open.org/cacao/coordinates/v1.0/csd01/coordinates-v1.0-csd01.html. Latest version: https://docs.oasis-open.org/cacao/coordinates/v1.0/coordinates-v1.0.html.",
       "url": "https://docs.google.com/document/d/1eWRxX3kKELOU_08ee013vDRrWYRu9JqS2LIt4Nk-F10/edit"
     }
   ]
 }
```

## JSON Validation Schemas

The JSON validation schemas are available in the [schemas directory](/schemas/).

## Use Case Example

The complete example encorporating the CACAO Coordinates specifications can be found here: [Full playbook with extension](/examples/playbook--cb11f617-6099-4a0d-9dd5-9d27f79c2194.json).

## Breaking Down of the Use Case

### 1. Providing the Extension Definitions

The `extension_definitions` property hold all the extensions utilized in the current playbook.  

```JSON
"extension_definitions": {
    "extension-definition--d03cf830-2e1a-49b4-a5ee-4bfa704f506a": {
    "type": "extension-definition",
    "name": "CACAO canvas",
    "description": "Extension definition for the Canvas size in which a CACAO playbook is graphically represented/visualized.",
    "created_by": "identity--5abe695c-7bd5-4c31-8824-2528696cdbf1",
    "schema": "placeholder for JSON Schema in CACAO TC Github Repo.",
    "version": "1.0.0",
    "external_references": [
        {
        "name": "CACAO Coordinates Specification.",
        "description": "Specification for CACAO Playbooks Canvas and Coordinates extensions.",
        "source": "[CACAO-Coordinates-Schema-v1.0] CACAO Coordinates Schema Version 1.0. Edited by Vasileios Mavroeidis and Mateusz Zych. 07 November 2023. OASIS Committee Specification Draft 01. https://docs.oasis-open.org/cacao/coordinates/v1.0/csd01/coordinates-v1.0-csd01.html. Latest version: https://docs.oasis-open.org/cacao/coordinates/v1.0/coordinates-v1.0.html.",
        "url": "https://docs.google.com/document/d/1eWRxX3kKELOU_08ee013vDRrWYRu9JqS2LIt4Nk-F10/edit"
        }
    ]
    },
    "extension-definition--418ee24c-9cb1-46d9-afa5-309e01aabc7f": {
    "type": "extension-definition",
    "name": "CACAO coordinates",
    "description": "Extension definition for Coordinates allowing CACAO Playbooks to be graphically represented on a canvas.",
    "created_by": "identity--5abe695c-7bd5-4c31-8824-2528696cdbf1",
    "schema": "placeholder for JSON Schema in CACAO TC Github Repo.",
    "version": "1.0.0",
    "external_references": [
        {
        "name": "CACAO Coordinates Specification",
        "description": "Specification for CACAO Playbooks Canvas and Coordinates.",
        "source": "[CACAO-Coordinates-Schema-v1.0] CACAO Coordinates Schema Version 1.0. Edited by Vasileios Mavroeidis and Mateusz Zych. 07 November 2023. OASIS Committee Specification Draft 01. https://docs.oasis-open.org/cacao/coordinates/v1.0/csd01/coordinates-v1.0-csd01.html. Latest version: https://docs.oasis-open.org/cacao/coordinates/v1.0/coordinates-v1.0.html.",
        "url": "https://docs.google.com/document/d/1eWRxX3kKELOU_08ee013vDRrWYRu9JqS2LIt4Nk-F10/edit"
        }
    ]
    }
}
```

### 2. Use the Canvas Extension

The `playbook_extensions` property is used to extend the playbook object (metadata) itself.
We are using the CACAO Canvas extension to define the canvas size for the visualized playbook.

```JSON
"playbook_extensions": {
    "extension-definition--d03cf830-2e1a-49b4-a5ee-4bfa704f506a": {
    "type": "canvas",
    "canvas_width": 500,
    "canvas_height": 300
    }
}
```

### 3. Use the Coordinates Extension

The CACAO Coordinates Extension can be used in all workflow steps, and agent and targets.
The code snippet below, presents the extension of a workflow step, in particular the switch case workflow step, through the `step_extension` property using the CACAO Coordinates Extension.

```JSON
"step_extensions": {
    "extension-definition--418ee24c-9cb1-46d9-afa5-309e01aabc7f": {
        "type": "coordinates",
        "x": 40,
        "y": 30,
        "outgoing_connections": [
            {
                "type": "connection",
                "connection_type": "cases",
                "case": "1",
                "x": ["70", "70"],
                "y": ["30", "50"]
            },
            {
                "type": "connection",
                "connection_type": "cases",
                "case": "2",
                "x": ["50", "80"],
                "y": ["80", "50"]
            },
            {
                "type": "connection",
                "connection_type": "cases",
                "case": "default",
                "x": ["60", "90"],
                "y": ["40", "70"]
            },
            {
                "type": "connection",
                "connection_type": "on-completion",
                "x": ["40", "90"],
                "y": ["30", "30"]
            }
        ]
    }
}
```

## Resources

- [CACAO-Coordinates-Schema-v1.0]
CACAO Coordinates Schema Version 1.0. Edited by Vasileios Mavroeidis and Mateusz Zych. 07 November 2023. OASIS Committee Specification Draft 01. https://docs.oasis-open.org/cacao/coordinates/v1.0/csd01/coordinates-v1.0-csd01.html. Latest version: https://docs.oasis-open.org/cacao/coordinates/v1.0/coordinates-v1.0.html.
- [CACAO-Security-Playbooks-v2.0]
CACAO Security Playbooks Version 2.0. Edited by Bret Jordan and Allan Thomson. 17 May 2023. OASIS Committee Specification Draft 02. https://docs.oasis-open.org/cacao/security-playbooks/v2.0/csd05/security-playbooks-v2.0-csd05.html. Latest version: https://docs.oasis-open.org/cacao/security-playbooks/v2.0/security-playbooks-v2.0.html.
