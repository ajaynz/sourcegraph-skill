# Common Search Examples

Real-world search examples for common tasks.

## Finding Implementations

**"Where is authentication handled?"**
```
sg_nls_search: "repo:^github.com/org/repo$ authentication middleware validation"
```

**"How do we make API calls?"**
```
sg_keyword_search: "repo:^github.com/org/repo$ fetch\|axios\|http\.request"
```

**"Find all database queries"**
```
sg_keyword_search: "repo:^github.com/org/repo$ \.query\(\|\.execute\("
```

## Understanding Flow

**"How does user signup work end-to-end?"**
```
sg_deepsearch_read: "Trace the user signup flow from form submission to database creation"
```

**"What happens when a payment fails?"**
```
sg_deepsearch_read: "How does the system handle failed payment attempts?"
```

## Debugging

**"Find where this error is thrown"**
```
sg_keyword_search: "repo:^github.com/org/repo$ 'User not found'"
sg_find_references: Find all usages of the error constant
```

**"What changed in authentication recently?"**
```
sg_diff_search: repos=["github.com/org/repo"] pattern="auth" after="2 weeks ago"
```

## Finding Patterns

**"How do other features handle validation?"**
```
sg_nls_search: "repo:^github.com/org/repo$ input validation schema"
```

**"Find examples of pagination"**
```
sg_keyword_search: "repo:^github.com/org/repo$ offset\|limit\|cursor\|pageToken"
```

## Tracing Dependencies

**"What uses this utility function?"**
```
sg_find_references: repo="github.com/org/repo" path="src/utils/format.ts" symbol="formatDate"
```

**"Where is this type defined?"**
```
sg_go_to_definition: repo="github.com/org/repo" path="src/api/handler.ts" symbol="UserResponse"
```
