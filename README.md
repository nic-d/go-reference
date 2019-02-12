### What?
I've decided to pick up Go (golang), and I need to keep a doc to keep track of some things I might need to come back to later.

#### Values
- Variables obviously hold values. But they can also hold channels, functions, methods, maps, slices, and pointers.
- Values passed to a function are copied in memory. Oh and it's worth mentioning that strings in memory are immutable.
Because strings are immutable, whenever it's modified in memory, it's then copied.
- Arrays are passed by value.
- Passing a slice costs the same as passing a string (16 bytes on a 64 bit machine), no matter how large the slice is.
- Slices aren't copied when modified because they're mutable, unlike strings.
- Variables that have no references or are out of scope are removed by the GC.
- A Go array is a fixed-length collection of items with the same data type.
- Arrays are mutable.
- Arrays can't change length.
- When you slice an array, you won't get an array back, you'll get a slice.
- Honestly, you'll probably use slices more than arrays...
- Slices are essentially references to hidden arrays.

Creating an array:
```go
// Create an array with the length 1, containing strings
[1]string
[1]string{"hello"}

// Also, you can do this cool thing, which lets Go calculate the length of the array for us:
// By using Ellipsis, Go will calculate that this string is 2 in length.
[...]string{"hello", "world"}
```
- A slice is variable-length, and like arrays, contain data of the same type.

Creating a slice:
```go
[]string{"hi"}
```

- A map is a collection of key-value pairs, and the keys must be unique.

Creating a map:
```go
map[string]string{"hello": "world"}
map[string]int{"hello": 1}
```
