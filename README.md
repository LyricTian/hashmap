# hashmap

[![GoDoc](https://img.shields.io/badge/api-reference-blue.svg?style=flat-square)](https://godoc.org/github.com/tidwall/hashmap)

A simple and efficient hashmap package for Go using the
[`xxhash`](http://www.xxhash.com) algorithm,
[open addressing](https://en.wikipedia.org/wiki/Hash_table#Open_addressing), and
[robin hood hashing](https://en.wikipedia.org/wiki/Hash_table#Robin_Hood_hashing).

This is an alternative to the standard [Go map](https://golang.org/ref/spec#Map_types).

# Getting Started

## Installing

To start using `hashmap`, install Go and run `go get`:

```sh
$ go get -u github.com/tidwall/hashmap
```

This will retrieve the library.

## Usage

The `Map` type works similar to a standard Go map, and includes four methods:
`Set`, `Get`, `Delete`, `Len`.

```go
var m hashmap.Map
m.Set("Hello", "Dolly!")
val, _ := m.Get("Hello")
fmt.Printf("%v\n", val)
val, _ = m.Delete("Hello")
fmt.Printf("%v\n", val)
val, _ = m.Get("Hello")
fmt.Printf("%v\n", val)

// Output:
// Dolly!
// Dolly!
// <nil>
```

## Contact

Josh Baker [@tidwall](http://twitter.com/tidwall)

## License

Source code is available under the MIT [License](/LICENSE).
