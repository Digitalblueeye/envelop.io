# capsule.io

[![godoc](https://img.shields.io/badge/godoc-reference-blue.svg)](http://godoc.org/github.com/rucuriousyet/capsule.io)

The little library for fetching application secrets!

## Usage

Here is an example capsule file
```
key=value
orange=a sweet orange fruit
foo=bar

```

***

```Go
package main

import (
  "fmt"

  caps "github.com/rucuriousyet/capsule.io"
)

func main() {
  /* 
    Since no file was specified, capsuleio.Get() will look in the project directory 
    for a *.capsule file. If you would like to specify a file to use, add the following
    line before any calls to Get().

    caps.Open("mycapsulefile.capsule")
  */

  fmt.Println(caps.Get("key")) //=> value
}

```

## Installation
```
go get github.com/rucuriousyet/capsule.io
```

Thanks for using Capsule! Feel free to reach out with questions, feature requests and more!
