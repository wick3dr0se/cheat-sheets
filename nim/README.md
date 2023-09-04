Let's learn Nim

## Resources
### Beginner Guides
[Nim by Example](https://nimbyexample.com/index.html)  
[Nim Tutorial](https://nim-lang.org/docs/tut1.html)  
[Nim Basics](https://narimiran.github.io/nim-basics/)   
[Nim Programming Book](https://github.com/StefanSalewski/NimProgrammingBook/blob/master/nimprogramming.adoc)

### Intermediate Guides
[Nim by Example](https://nim-by-example.github.io) yep, there is another one  
[Learn Nim in 5 minutes](https://learnxinyminutes.com/docs/nim/)  
[Nim Manual](https://nim-lang.org/docs/manual.html)

### Refrences
[Nim Docs](https://nim-lang.org/documentation.html)  
[Nim Language Index](https://nim-lang.org/docs/theindex.html#%60%7B%7D%3D%60)  

### Sandbox
[Play Nim](https://play.nim-lang.org/)

---

<details open><summary><h3>:speech_balloon: Comments</h3></summary>

```nim
# comment
## documentation comment
#[ multi-line 
comment ]#
```

---

</details>
<details open><summary><h3>:exclamation: Operators</h3></summary>

## arithmetic Operators
calculate numerical values
```nim
+ # add
- # subtract
* # multiply
/ # divide
^ # power
```

## assignment Operators
define a value
```nim
= # assign
+= # add, assign
```
## logical Operators
test if conditions are true or not
```nim
# following operators return true, if:
and # both conditions are true
or # condition(s) is true
xor # a condition is true and other is not
not # condition is false (accepts a single condition)
```
## relational operators
test the relation between two comparable conditions
```nim
== # is equal   != # not equal
> # greater than   >= # greater or equal
< # lesser than   <= # less or equal
```

---

</details>
<details open><summary><h3>:label: Data Types</h3></summary>

data types declare how variable values are interpreted
## bool
true/false
```nim
var <santa>: bool = <true>
```
## int
integer
```nim
var <n>: int = 1
```
## float
floating-point number
```nim
var <n>: float = <1.1>
```
## char
a single character (single quotes)
```nim
var <i>: char = '<a>'
```
## string
character array (double quotes)
```nim
var <distro>: string = "<Arch Linux>"
```

---

</details>
<details open><summary><h3>:blue_book: Variables</h3></summary>

## var
define (& declare) a data type of mutable value
```nim
# declare variable
var <n>: int

# define variable
<n> = 1

# declare & define variable
var <n>: int = 1

# multi-variable declaration
var <n>, <i>: int

# declare variable block
var
  <n>: int
  <name: char
```

## const
define a constant of immutable value (read at compile time)
```nim
# define constant
const Pi = 3.14
  
# define constant block
const
  Pi = 3.14
  four = 4
  apple = "red"
```

## let
declares & defines a(n existing) variable to an immutable value (read at runtime)
```nim
let n = 2
```

_const or let should always be preferred unless variable must be mutable_

---

</details>
<details open><summary><h3>:books: Types</h3></summary>

## array
a collection of strings
```nim
type
  TwoArgs = array[2, strings]
```

## enum
a group of constants
```nim
type
  Signals = enum
    sigQuit = 3, sigAbort = 6, sigKill = 9
```

---

</details>
<details open><summary><h3>:balance_scale: Statements</h3></summary>

## if
branch control flow, good for 3/4 expressions
```nim
if Pi == 3.14:
  echo "Let's have Pi"
elif apple == red:
  echo "Apples are red"
else:
  echo "Neither apples are read nor Pi equal 3.14"
```

## when
same as if, except with constants and statement remains in the same scope. only the true expression gets seen by the compiler
```nim
when apple == red:
  return true
elif apple == orange:
  return false
```

## case
multi-branch control flow, good for more than 3 expressions
```nim
case "Pi":
  of "blueberry":
    "fail"
  of "3.14":
    "pass"
  else:
    "impossible"
```

_control flow statements will be executed only if some condition is satisfied_

---

</details>
<details open><summary><h3>:infinity: Loops</h3></summary>

## for
iterate until condition is met
```nim
for i in 1 .. 10:
  echo i
```

## while
execute until condition is false
```nim
while true:
  echo "This will never stop"
```

---

</details>
<details open><summary><h3>:clipboard: Procedures</h3></summary>

## proc
a re-usable piece of code (function)
```nim
proc onOff(reply: char): bool =
  echo reply, " [y/n]"
  if reply == y:
    return true
  else:
    return false
    
onOff(y) # true
```
</details>
