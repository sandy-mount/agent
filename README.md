# Agent Vocabulary

A simple vocabulary for describing Agents and agency relationships.

## Overview

This vocabulary defines:

- The concept of an Agent - an entity that has agency and can act independently.
- A property to link any Thing to an Agent that has agency over it.

## Namespace

The namespace for this vocabulary is `https://w3id.org/agent#`.

## Classes

### Agent

An entity that has agency - the capacity to act independently and make free choices.

## Properties

### agent

Links a Thing to an Agent.

- **Domain:** `owl:Thing`
- **Range:** `agent:Agent`

## Example Usage in JSON-LD

Here is an example of a JSON document using this vocabulary:

```json
{
  "@context": {
    "@vocab": "https://w3id.org/agent#"
  },
  "@type": "Person",
  "@id": "https://example.org/people#jane_smith",
  "agent": [
    {
      "@type": "Agent",
      "@id": "https://example.org/agents#robot1",
      "name": "Kitchen Assistant"
    },
    {
      "@type": "Agent",
      "@id": "https://example.org/agents#robot2",
      "name": "Garden Helper"
    }
  ]
}
```

### Explanation:

- The `@context` specifies the vocabulary (`https://w3id.org/agent#`) and additional namespaces.
- The `@id` is used to define the identifier of the entity (`https://example.org/people#jane_smith`).
- The `@type` is used to define the type of entity (`Person`).
- The `agent` property is used to link the person to the agents they own.

This makes JSON-LD highly flexible and suitable for building interoperable data models while maintaining backward compatibility.

## Status

This document is a draft vocabulary specification.

## License

This vocabulary is available under the [MIT License](https://opensource.org/licenses/MIT).
