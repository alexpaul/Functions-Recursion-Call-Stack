# Functions, Recursion and the Call Stack

Functions, recursion and the call stack. 


```swift 
func power(x: Int, y: Int) -> Int {
  guard y > 1 else {
    return x
  }
  return x * power(x: x, y: y - 1)
}

print(power(x: 2, y: 3)) // 8
```
