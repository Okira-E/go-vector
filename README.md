# Vector in Go

`Vector` is a simple implementation of a generic vector data structure in Go. It provides higher level functions to manipulate the vector.

## Installation

It will always be easier to just copy the code and paste it in your project.

## Example

```go
v := NewVec(1, 2, 3, 4, 5, 6, 7, 8, 9, 10)

// Get the length of the vector
fmt.Println("Length:", v.Len())

// Append a value
v.Push(6)
v.Unshift(0)

// Remove and print the last value
fmt.Println("Popped:", v.Pop())

// Print the vector using ForEach
v.ForEach(func (index int, value int) {
    fmt.Println("Index:", index, "Value:", value)
})

newVec := v.Range(0, 5).Map(func (_ int, value int) int {
    return value * 2
})

filteredVec := v.Filter(func (index int, value int) bool {
    return value % 2 == 0
})
```

## License

This project is licensed under the Unlicensed License - see the [UNLICENSE](UNLICENSE) file for details

## Contributing

Feel free to open a pull request or an issue if you want to contribute to this project.