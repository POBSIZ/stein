# stein

Stein Language

## Syntax

### Define Variable

```stein
let x = 10
let name = "stein"
```

### Define Function

```stein
fn add(a, b) => a + b
let double = fn (x) => x * 2
```

### Call Function

```stein
print(double(add(2, 3)))
```

### Condition

```stein
print(if x > 0 then "positive" else "non-positive")
if x == 0 then print("zero")
x == 1 ? print("one") : void
```

### List & HOF

```stein
let nums = [1, 2, 3, 4]

map(double, nums)
filter((fn (x) => x > 2), nums)
```

### Parallelism

```stein
spawn(fn => print("Hello Stein!"))

spawn(fn => {
  let x = 1
  print(x)
})
```

### Block

```stein
{
  let a = 1
  let b = 2
  return a + b // return this line
}
```

### Sample

```stein
let greet = fn (name) => print("Hello, " + name)

let names = ["Alice", "Bob", "Carol"]

map(greet, names)

spawn(fn => print("running in parallel"))
```

## Structure

- Lexer
- Parser
- AST
- Interpreter
- Environment
- Garbage Collector
- Parallelism