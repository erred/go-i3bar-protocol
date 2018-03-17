# go-i3bar-protocol [![GoDoc][1]][2] [![Build Status][3]][4] [![Go Report Card][5]][6] [![License: MIT][7]][8]

[1]: https://godoc.org/github.com/seankhliao/go-i3bar-protocol?status.svg
[2]: https://godoc.org/github.com/seankhliao/go-i3bar-protocol
[3]: https://img.shields.io/travis/seankhliao/go-i3bar-protocol.svg?style=flat-square
[4]: https://travis-ci.org/seankhliao/go-i3bar-protocol
[5]: https://goreportcard.com/badge/github.com/seankhliao/go-i3bar-protocol?style=flat-square
[6]: https://goreportcard.com/report/github.com/seankhliao/go-i3bar-protocol
[7]: https://img.shields.io/badge/License-MIT-blue.svg?longCache=true&style=flat-square
[8]: LICENSE

Go types for use with [i3bar](https://i3wm.org/docs/i3bar-protocol.html)

## Install

```bash
go get github.com/seankhliao/go-i3bar-protocol
```

## Example

```go
package main

import (
        "github.com/seankhliao/go-i3bar-protocol"
        "encoding/json"
        "fmt"
        "os"
)

func main() {
        e := protocol.NewEncoder(os.Stdout)
        e.Encode(protocol.MinimalHeader())
        e.BeginArray()

        for {
                var blocks []protocol.Block
                // fill blocks
                e.Encode(blocks)
        }
}
```

## License

The MIT License (MIT) - see [`LICENSE`](LICENSE) for more details
