<!--
Title: Storage API Go
Description: Storage api to support Pure and Solidfire Storage Arrays
Author: kgrvamsi
-->

# StorageAPI

This Library supports Pure Storage array and Solidfire(Future scope)

[![GoDoc](https://godoc.org/github.com/kgrvamsi/storageapi?status.svg)](https://godoc.org/github.com/kgrvamsi/redfishapi)
[![Go Report Card](https://goreportcard.com/badge/github.com/kgrvamsi/storageapi)](https://goreportcard.com/report/github.com/kgrvamsi/storageapi)

## Usage

```go
//main.go
package main

import "fmt"
import "github.com/kgrvamsi/storageapi"

func main() {
    client, err := NewStorageClient("192.168.1.115", "admin", "admin", "", "1.17")

	array, err := client.FetchArrayInfo()
	if err != nil {
		fmt.Println(err)
	}
	fmt.Println(array)
}
```
