{
	"title": "add-package",
	"description": "[Spider to DLT] Adds a package to the spider TODO list. This can be a yet unknown package, or (?) a package whose data has been outdated.",
	"type": "object",
	"properties": {
		"url": {
			"type": "string"
		}
	},
	"additionalProperties": false,
	"required": ["url"]
}

{
	"title": "send-package",
	"description": "[DLT to Spider] Send package",
	"type": "object",
	"properties": {
		"url": {
			"type": "string"
		}
	},
	"additionalProperties": false,
	"required": ["url"]
}

{
	"title": "send-trust-facts",
	"description": "[Spider to DLT] Send trust facts",
	"type": "object",
	"properties": {
		"url": {
			"type": "string"
		},
		"user-id": {
			"type": "number"
		},
		"trust-facts": {
			"type": "array",
			"items": {
				"type": "array",
				"prefixItems": {
					"type": "string",
					"type": "string"
				},
				"items": false
			}
		}
	},
	"additionalProperties": false,
	"required": ["url", "user-id", "trust-facts"]
}
