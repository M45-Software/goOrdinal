# ordinal

A dependency-free Go library for converting `int64` values to English ordinal words.

## Install

```sh
go get github.com/Distortions81/ordinal
```

## Usage

```go
package main

import (
	"fmt"

	"github.com/Distortions81/ordinal"
)

func main() {
	fmt.Println(ordinal.NumberToOrdinal(342))  // Three hundred forty-second
	fmt.Println(ordinal.NumberToOrdinal(-21))  // Minus twenty-first
	fmt.Println(ordinal.NumberToOrdinal(0))    // Zeroth
}
```

`NumberToOrdinal` supports the full `int64` range, including negative values and
`math.MinInt64`. Output begins with a capital letter, uses hyphens for compound
tens, omits “and,” and uses English short-scale names such as billion and trillion.

## Migrating from goCardinal

Replace imports of `github.com/Distortions81/goCardinal` with
`github.com/Distortions81/ordinal` and change the package qualifier from
`goCardinal` to `ordinal`. The `NumberToOrdinal` function and its output are unchanged.

## License

[MIT](LICENSE)
