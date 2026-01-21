# Debugging an Issue

When tracking down bugs, search systematically from symptom to cause.

## Checklist

```
Task Progress:
- [ ] Search for error
- [ ] Find where thrown
- [ ] Understand context
- [ ] Check recent changes
```

## Steps

### 1. Search for the Error

```
sg_keyword_search: "repo:X 'INVALID_TOKEN_ERROR'"
```

Search for:
- Exact error message text
- Error codes or constants
- Exception class names
- Log message patterns

### 2. Find Where It's Thrown

```
sg_find_references: Trace the error symbol
```

Locate all places this error can originate:
- Direct throw statements
- Wrapper functions
- Error factories

### 3. Understand the Context

```
sg_deepsearch_read: "When is INVALID_TOKEN_ERROR thrown and how should it be handled?"
```

Get deeper understanding of:
- Conditions that trigger the error
- Expected handling patterns
- Related error types

### 4. Check Recent Changes

```
sg_diff_search: "repo:X INVALID_TOKEN_ERROR"
sg_commit_search: repos=["X"] messageTerms=["token", "auth"]
```

Look for recent modifications that might have introduced the bug.

## Tips

- Extract exact symbols from stack traces
- Errors often have multiple throw sites—check all of them
- Recent changes are prime suspects
- Check if error handling changed, not just the error source
