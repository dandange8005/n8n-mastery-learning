# n8n Expression Cheat Sheet

Quick reference for common n8n expressions.

## Accessing Data

```javascript
// Current item's data
{{ $json.fieldName }}

// Specific item by index
{{ $item(0).$json.fieldName }}

// From previous node
{{ $node["Node Name"].json.fieldName }}

// All items from previous node
{{ $node["Node Name"].json }}
```

## String Operations

```javascript
// Concatenation
{{ $json.firstName + " " + $json.lastName }}

// Uppercase/Lowercase
{{ $json.text.toUpperCase() }}
{{ $json.text.toLowerCase() }}

// Substring
{{ $json.text.substring(0, 10) }}

// Replace
{{ $json.text.replace("old", "new") }}

// Trim whitespace
{{ $json.text.trim() }}
```

## Date Operations

```javascript
// Current date/time
{{ $now }}

// Format date
{{ $now.format("YYYY-MM-DD") }}
{{ $now.format("DD/MM/YYYY HH:mm:ss") }}

// Add/subtract time
{{ $now.plus(1, "day") }}
{{ $now.minus(2, "hours") }}

// Parse date
{{ DateTime.fromISO($json.dateString) }}
```

## Array Operations

```javascript
// Length
{{ $json.items.length }}

// First/Last item
{{ $json.items[0] }}
{{ $json.items[$json.items.length - 1] }}

// Map array
{{ $json.items.map(item => item.name) }}

// Filter array
{{ $json.items.filter(item => item.active) }}

// Find item
{{ $json.items.find(item => item.id === 123) }}
```

## Conditional Logic

```javascript
// Ternary operator
{{ $json.age >= 18 ? "Adult" : "Minor" }}

// Null coalescing
{{ $json.optionalField ?? "Default Value" }}

// Multiple conditions
{{ $json.score > 90 ? "A" : $json.score > 80 ? "B" : "C" }}
```

## Number Operations

```javascript
// Math operations
{{ $json.price * 1.2 }}
{{ Math.round($json.value) }}
{{ Math.floor($json.value) }}
{{ Math.ceil($json.value) }}

// To fixed decimal
{{ $json.price.toFixed(2) }}

// Parse number
{{ parseInt($json.stringNumber) }}
{{ parseFloat($json.stringNumber) }}
```

## JSON Operations

```javascript
// Parse JSON string
{{ JSON.parse($json.jsonString) }}

// Stringify object
{{ JSON.stringify($json.object) }}

// Pretty print
{{ JSON.stringify($json.object, null, 2) }}
```

## Useful Patterns

```javascript
// Check if value exists
{{ $json.field !== undefined && $json.field !== null }}

// Default value
{{ $json.field || "default" }}

// Safe navigation
{{ $json.user?.address?.city }}

// Generate random ID
{{ $now.toMillis() }}-{{ Math.random() }}
```

---

For more expressions, see the [n8n Expressions Documentation](https://docs.n8n.io/code-examples/expressions/)
