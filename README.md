## SwiftTips
Interesting things from Swift language

### Optionals

#### Assign value only when current value is not nil
```
var maybe: Int? = nil
maybe? = 42
// maybe = nil
maybe = 7
maybe? = 42
// maybe = 42
```

#### Mapping optionals
```
let maybe: Int? = 7
let mappedMaybe = maybe.map { $0 * 6 }
```

#### Looping over non-nil values
```
let maybeValues: [Int?] = [1, 2,3,nil]
for case let value? in maybeValues {
    // here value is unwrapped, nil values are filtered out
}

// it's equivalent to:
for case let .some(value) in maybeValues {
  // 
}

// we can also loop over every nil in the array
for case let .none in maybeValues {
  // 
}

// or using shorthand
for case nil in maybeValues {
  // 
}
```

#### Comparing equality of optional and non-optional values
When comparing Optional vs Non-Optional Swift will promote Non-Optional to Optional in order to apply equality check on two Optionals.

```
let maybe7: Int? = 7
if maybe7 == 7 {
    print("it's seven!")
}
```

