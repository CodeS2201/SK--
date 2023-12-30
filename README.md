# SK--
Repository for the programming language SK++ developed by Sourish Tilwankar and Kriday Lalwani
<br>
## Intro to SK++
SK++ was developed by two 14 year old wannabe devs in their free time instead of actually studying. <br>
This is just a personal project for now, but might be scaled to be a real language one day. <br>
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
Loops in SK++ consist of the traditional **while** and **for** loops, which can be initiated with keywords **till** and **untill** respectively.
### While Loop
```
run main() {
  num i = 0;
  till(i <= 10) {
    writeNL(i);
    i++; // i = i + 1
  }
}
```

> **NOTE**: Here, we have used the function **writeNL()** to print the output with the '\n' newline character.

### For Loop
```
run main() {
  untill(num i = 0; i <= 10; i++) {
    writeNL(i);
  }
}
```
