# GO MODULE

# Create a directory outside of your GOPATH, and optionally initialize VCS:

$ mkdir -p /tmp/scratchpad/repo
$ cd /tmp/scratchpad/repo
$ git init -q
$ git remote add origin https://github.com/my/repo

# Initialize a new module:

$ go mod init github.com/my/repo

## go: creating new go.mod: module github.com/my/repo

# Write your code:

$ cat <<EOF > hello.go
package main

import (
    "fmt"
    "rsc.io/quote"
)

func main() {
    fmt.Println(quote.Hello())
}
EOF

# Build and run:

$ go build -o hello
$ ./hello

#### Hello, world.

$ cat go.mod

module github.com/my/repo

require rsc.io/quote v1.5.2