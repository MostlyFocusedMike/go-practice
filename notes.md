# Golang Notes 
These are the overall notes, compiled from various sources.

# CodeCademy Course 
------------------------------------------------------------------------------------------------------------
# Part 1: Basics 
[Cheatsheet](https://www.codecademy.com/learn/learn-go/modules/learn-go-introduction/cheatsheet)

Go is a compiled language so in order to run your program you either need to `build` or `run`

```bash
go build main.go
```

This will create an executable: 

```bash
/codecademy-course git:(main) ls
  main    main.go
```

Which you can then call with `./main`

You can also use the `run` command. This will execute the program, but not create the executable. 

## Packages 

Projects can contain many `.go` files, organized into packages. Each package is like a directory: `.go` files to do with one part of your program can go in one package, other `.go` files to do with something else can go into another package. If we were writing a calculator program, we could put the files for the calculation in package calc and the files for input & output in package `io`.

The first line of a file is the package declaration, followed by white space. Then we have the `import` statement. This can either be a single string or () with several new line split strings like this: 

```go 
import "fmt"

import (
  "fmt"
  "math"
)
```

You can also alias package names like this: 

```go 
package main

import (
  "fmt"
  t "time"
)

func main() {
  fmt.Println(t.Now())
	fmt.Println("Hello World")
}
```

## The main function and functions 
All go programs have a main function. It belongs in the main package, and doesn't get called by you. You define functions using the `func` keyword. It has parens for arguments (though we don't know how to pass them in yet without knowing types).   

The `main` function is what makes it acutally compile an executable.

## comments 
Same as js, // and /* */

## Go doc command 
In the command line you can run `go doc [package]` and Go will print out information about it 

## Go doc command 
In the command line you can run `go doc [package]` and Go will print out information about it. You can also use methods in the package like `go doc fmt.Println`

--------------------------------------------------------------------------------------------------------------------------------
## Part 2: Variables 
[Cheatsheet](https://www.codecademy.com/learn/learn-go/modules/learn-go-variables-and-formatting/cheatsheet)

- declare variables for changable values and const for non changing values
```go
// constant named value
const pi = 3.14159

// variable named value
var radius = 6

// declare the 0 value prior to defining 
var fruit string
fruit = "apple"

// the 0 values for strings is ''
// or define at the same time 
var fruit string = "apple"

// you can also skip the types
var fruit = "apple"

// or use := shorthand assigment which infers type and skips var
fruit := "apple"
```

## Data Types 
the three basic types for numbers are integers (int), floats (float) and strings (str). Also complex (complex) numbers that are imaginary numbers. Which is neat
- the ints can be signed (negative and positive) or unsigned (positive only)
- there's a cool table picture


