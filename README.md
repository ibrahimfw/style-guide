
# Freshworks OpenAPI 2.0 Style Guide

Lint rules to validate Open API 2.0 Specification using [Spectral](https://stoplight.io/open-source/spectral/). This extends ***spectral:oas*** package and adds custom rules on top of it.

# Usage

## Extending this style guide

### YAML

    extends:
	  - https://unpkg.com/fw-style-guide
	rules:
	  ...

### JSON


     {
        "extends": [
            "https://unpkg.com/fw-style-guide"
        ],
        "rules": {
            ...
        }
    }

# Rules
Some rules are used from ***spectral:oas*** as it is and overridden the severity to **ERROR**. Rules that are not extended from ***spectral:oas*** will have prefix `fw-`.

> Severity is set to **ERROR** for all rules defined below. Individual  
> projects can override severity level to suit their needs.

## info-description

OpenAPI object info `description` must be present and non-empty string.

## info-contact

Info object should contain `contact` object.

## operation-tags

Operation should have non-empty `tags` array.

## operation-tag-defined

Operation tags should be defined in global tags.

## operation-operationId

Operation should have an `operationId`.

## fw-info-license

Info object should contain `license` object

## fw-operation-summary

Each operation should have `summary`

## fw-schema-properties-example

Schema properties should have an example value defined

## fw-properties-underscore-case

Schema properties should be in underscore case

## fw-ensure-no-legacy-tags

Tags should not have legacy in its name

## fw-path-kebab-case

Path should be in kebab case.

> Private APIs follows the convention of `/api/_/...` . One underscore (`_`) followed by `/api/` is allowed for private APIs as an exception.

## fw-path-param-underscore-case

Path parameter should be in underscore case

## fw-query-param-underscore-case

Query parameter should be in underscore case

## fw-form-param-underscore-case

Form data parameter should be in underscore case