Javascriptish Swift Arrays
==========================

Extension to make swift arrays feel more JavaScript-like. Under construction.


push
----
Adds multiple elements to an array 

```swift
var fruits = ["Banana", "Orange"]
fruits.push("Apple")
fruits.push("Kiwi", "Papaya")

// fruits == ["Banana", "Orange", "Apple", "Kiwi", "Papaya"]
```


pop
----
Removes and returns the last element of an array 

```swift
var fruits = ["Apple", "Banana", "Orange"]
var popped = fruits.pop()

// popped == "Orange"
// fruits == ["Apple", "Banana"]
```


shift
----
Removes and returns the first item of an array


```swift
var fruits = ["Banana", "Orange", "Apple", "Mango"]
var shifted = fruits.shift()				

// shifted == "Banana"
// fruits == ["Orange", "Apple", "Mango"]
```



unshift
----

Adds new elements to the beginning of an array:


```swift
var fruits = ["Banana", "Orange"]
fruits.unshift("Lemon","Pineapple")

// fruits == ["Lemon","Pineapple", "Banana", "Orange"]
```

concat
----

Joins multiple arrays. Method does not change the existing arrays, but returns a new array.


```swift
var yellowFruits = ["Banana", "Lemon"]
var otherFruits = ["Orange", "Apple"]
var allFruits = yellowFruits.concat(otherFruits)

// allFruits == ["Banana","Lemon", "Orange", "Apple"]
```

indexOf
----

Searches the array for the specified item, and returns its position. The search will start at the specified position, or at the beginning if no start position is specified, and end the search at the end of the array. Returns -1 if the item is not found. If the item is present more than once, the indexOf method returns the position of the first occurence.


```swift
var fruits = ["Banana", "Orange", "Apple", "Mango"]
var a = fruits.indexOf("Apple")

// a == 2

var fruits = ["Banana", "Orange", "Apple", "Mango", "Banana", "Orange", "Apple"]
var a = fruits.indexOf("Apple", startIndex:4)

// a == 6

```


join
----

Joins all elements of an array into a string


```swift
var fruits = ["Banana", "Orange", "Apple", "Mango"]
var result = fruits.join()

// result = "Banana,Orange,Apple,Mango"

var fruits = ["Banana", "Orange", "Apple", "Mango"]
var result = fruits.join(separator:" & ")

// result = "Banana & Orange & Apple & Mango"

```


slice
----

Returns the selected elements in an array, as a new array object. Method selects the elements starting at the given start argument, and ends at, but does not include, the given end argument. The original array will not be changed.

```swift
var fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"]
var myBest = fruits.slice(-3, -1)

// myBest == ["Lemon","Apple"]
```

splice
----

Adds/removes items to/from an array at position, and return the removed items.


```swift
var fruits = ["Banana", "Orange", "Apple", "Mango"]
var spliced = fruits.splice(index:2, howMany:1, elements: "Lemon", "Kiwi")

// spliced == ["Apple"]
// fruits == ["Banana","Orange","Lemon","Kiwi","Mango"]
```