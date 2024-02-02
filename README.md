# SK--
Repository for the programming language SK++ developed by Sourish Tilwankar and Kriday Lalwani
<br>
## Intro to SK++
SK++ is a modern programming language. It was built by us when we realized that there weren't many good abstract interfaces over low level workings of memory,
memory addresses, bitwise operations and pointers. These concepts are very necessary for memory management and efficiency. <br>
But, there stood a problem. Modern languages which use garbage collectors for memory management, are not very efficient. For such tasks near the hardware layer, we use languages like C and C++. The concepts in these languages for low-level control, are quite difficult to grasp, and allow for a huge range of errors. <br>
SK++ makes it easy to program such task, by providing a layer of abstraction which is very easy to learn. <br>
With SK++ you can build performant applications, iot devices, robots which need precision, etc.
## Basic Syntax
### Declaring our main method/function:
```
run main() {

}
```
you can use the keyword **'run'** to define a function.
<br>
### Hello, World! program
```
run main() {
  write("Hello, World!");
}
```
you can use the *write();* function to print to the standard output.
<br>
### Datatypes in SK++
Currently, there are four datatypes in SK++ being:
1. **num** - the number data-type, also known as int in other languages.
2. **txt** - the text data-type, also known as string in other languages.
3. **dec** - the decimal data-type, also known as float in other languages.
4. **binary** - the binary data-type, also known as boolean in other languages.

### declaring variables
To declare a variable, type the datatype followed by the variable's name, '=' symbol and then its value.
```
<datatype> variable_name = <value>
```

Examples:
```
run main() {
  num age = 14;
  txt language = "SK++";
  dec PI = 3.14;
  binary isCool = true
}
```

### Conditional Statements
You can write conditional statements using the check, check-alt and alt keywords.
```
run main() {
  num age = 14;
  check(age >= 18) {
    write("you are an adult");
  }
  check-alt(age > 0 && age < 18) {
    write("you are a minor");
  }
  alt {
    write("you can't possibly exist, can you?");
  }
}
```

## Loops
Loops in SK++ consist of the traditional **for** loop, which can be initiated with keyword **iterate**, and a new, simpler loop, the **untill** loop.
SK++ also provides an **each** loop to iterate over structures.
We can add conditional statements in the loop which runs untill the statement is true.
### untill Loop
```
run main() {
  num i = 0;
  untill(i is 10) {
    writeNL(i);
    increment(i);
  }
}
```

More conditionals in the loop:

```
run main() {
  num:mini i = 0;
  int:block[] myArray = [13, 5, 20, 14]; 
  untill(i is in myArray) {
    writeNL('loop is running!');
    increment(i);
  }
  // runs 6 times.
}
```

> **NOTE**: Here, we have used the function **writeNL()** to print the output with the '\n' newline character.

### For Loop
```
run main() {
  iterate(i from 1 to 10) {
    writeNL(i);
  }
}
```

### each loop
```
initialize MAP(txt, num):hash as hashmap;
hashmap.write('first', 1);
hashmap.write('second', 2);
hashmap.write('third', 3);
each(key, value in hashmap) {
  writeNL(key + ': ' + value);
}
```
