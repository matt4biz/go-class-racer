[![Run on Repl.it](https://repl.it/badge/github/matt4biz/go-class-racer)](https://repl.it/github/matt4biz/go-class-racer)

# Go class: Race condition example
This little program demonstrates a race condition; in theory, it should print 1000 but most likely never will on any multi-core machine.

```
$ go run .
947

$ go run .
943

$ go run .
947

$ go run .
958
```

Of course, the fix is either to use a sync.Mutex or sync.Atomic where the increment happens.
