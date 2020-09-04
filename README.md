# Functions, Recursion and the Call Stack

Functions, recursion and the call stack. 


#### Write a function that recursively calculates the `power()` of a given number. 

```swift 
func power(x: Int, y: Int) -> Int {
  // 1
  guard y > 1 else {
    return x
  }
  // 2
  return x * power(x: x, y: y - 1)
}

print(power(x: 2, y: 3)) // 8
```

1. Base case. 
2. Recursive call. 

#### Write a function that uses recursion to print the values of a Linked List. 

```swift 
class Node {
  var value: Int
  var next: Node?
  init(_ value: Int) {
    self.value = value
  }
}

let node1 = Node(1)
let node2 = Node(2)
let node3 = Node(3)

node1.next = node2
node2.next = node3

func printNode(_ node: Node?) {
  // 1
  guard let node = node else {
    return
  }
  // 3
  print("\(node.value)", terminator: " ") // 1 2 3 
  // 2
  printNode(node.next)
  // 4 
  //print("\(node.value)", terminator: " ") // 3 2 1
}

printNode(node1)
```

1. Base case 
2. Recursive call
3. Print value of current node 
4. If we were to print the node values after the function returns at each recursive call the values would be reversed. 

