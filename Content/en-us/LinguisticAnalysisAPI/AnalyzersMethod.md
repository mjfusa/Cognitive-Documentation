<!--
NavPath: Linguistic Analysis API
LinkLabel: Analyzers Method
Url: Linguistic-Analysis-API/documentation/AnalyzersMethod
Weight: 80
-->

# Analyzers Method

The **analyzers** REST API provides a list of analyzers currently supported by the service.
The response includes their [names](Analyzer-Names.md) and the languages supported by each (such as "en" for English).

## Request parameters
None

<br>

## Response parameters
Name | Type | Description
-----|------|--------------
languages | list of strings | list of two letter ISO language codes for which this analyzer can be used.
id   | string | unique ID for this analyzer
kind | string | the broad type of analyzer here
specification | string | the name of the specification used for this analyzer
implementation | string | description of the model and/or algorithm behind this analyzer

<br>
## Example
GET /analyzers

Response: JSON
```json
[
	{
		"id": "22A6B758-420F-4745-8A3C-46835A67C0D2",
		"languages": ["en"],
		"kind": "Constituency_Tree",  
		"specification": "PennTreebank3", 
		"implementation": "SplitMerge"
	}, 
	{
		"id" : "4FA79AF1-F22C-408D-98BB-B7D7AEEF7F04",
		"languages": ["en"],
		"kind": "POS_Tags", 
		"specification": "PennTreebank3", 
		"implementation": "cmm"
	},
	{
		"id" : "08EA174B-BFDB-4E64-987E-602F85DA7F72",
		"languages": ["en"],
		"kind": "Tokens", 
		"specification":"PennTreebank3", 
		"implementation": "regexes"
	} 
]
```
