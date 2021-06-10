# Differences between Kotlin and Swift

###### as seen as a Kotlin developer learning Swift

---

##### Work in progress. I am adding things as I come across them

## Resources

- [Swift and Kotlin: The Subtle Differences](https://willowtreeapps.com/ideas/swift-and-kotlin-the-subtle-differences)
  by Kyle Ohanian[@kohanian](https://github.com/kohanian)
- [Hacking With Swift](https://www.hackingwithswift.com/)
  by Paul Hudson [@twostraws](https://twitter.com/twostraws) has wonderful content

---

### Casting

With Kotlin—in most cases—there are extension functions that handle the cast, while in Swift you instantiate the with
the value that is being converted.

Kotlin

```kotlin
5.0.roundToInt()

5.toString()
```

Swift

```swift
Int(5.0.rounded())

String(5)
```

### String interpolation

```swift
let age = 20
print("Sam is \(age)")
```

### Extension functions

```swift
extension Int {
    func toRgb() -> Double{
        Double(self) / 255
    }
}
```