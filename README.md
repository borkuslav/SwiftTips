# SwiftTips
Interesting things from Swift language

# Optionals

Assign value only when current value is not nil:
```
var maybe: Int? = nil
maybe? = 42
// maybe = nil
maybe = 7
maybe? = 42
// maybe = 42
```

Mapping optionals:
```
let maybe: Int? = 7
let mappedMaybe = maybe.map { $0 * 6 }
```
