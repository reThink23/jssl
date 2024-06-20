# jssl
# Joel's Syntax Sugar Language

## Principles
- customizable with sensible defaults
- multiparadigm
- advanced strings (md, html)
- optional typed
- latex suport for fast utf-8 char retrieval
- zero based
- fraction support
- expressive error messages
- information & tips to optimize performance (if vs switch)
- compiled & interactive

## Basic Syntax
### Example
```js
name = 'Max'
name = "Max"

name?? // prints debug information about name

checked = year % 4 ? true : false // ternary operator

if !(i in list)?
  // do something
else?
  // do something different

if i not in list? {
// do something
} else? {
// do something different
}

while i <= len #
  // do iterate

while i <= len # {
// do iterate
}

for i in 1..N #
  // tabs required
  // do something

for i in 1..N # {
// otherwise use a statement block with '{' and '}'  
// do something
}

num = 1_000_000
fr = 1/7
decimal = dec(fr)
fr2 = frac(decimal)


fn|fun|func|function check() =>
  // do something

fn|fun|func|function check() => {
// do something
}

with open(file) as f =>
  line = f.readLine()

// Lambda functions
(x,y) => x+y

x,y = y,x

class sd extends Iteratable =>
  met|method construct()

record sd // basically a named dict, also known as record or dataclass

list = ["1.5", "-0.7", "3"]
l = float#(list) // [1.5, -0.7, 3]
l = list.map(float) // [1.5, -0.7, 3]

sum = add(...list)
```
Whenever tabs would be required, '{', '}' can be used to create a scoped statement block

```js

name = "John"
const name =  // same as val ref const -> value and reference are const

val const name = // value is const, reference is not
ref const name = // reference is const, value not
```
not explicitly as constant declared variable which does not change will be converted to constant

## Naming Convention
- unicode characters can be used as variable names
camelCase

