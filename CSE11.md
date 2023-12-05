# CSE11 Introduction to Programming and Computational Problem-Solving

## Introduction

> `Foo.java`:
>
> ```java
> public class Foo {
>   		public static void main(String[] args) {
>     				System.out.println(“Hello world”);
> 		}
> }
> ```
>
> `Foo` is class name (capitalized first letter).

### Compile

Translate human-readable Java language program into an equivalent program in a language closer to what the computer can understand.

> ```shell
> $ javac Foo.java
> ```
>
> Generate `Foo.class` file (binary).
>

### Run

Use Java applications (with a `main()` method).

> ```shell
> $ java Foo
> ```
>
> Can use shortcut to combine compile and run, but not recommended:
>
> ```shell
> $ java Foo.java
> ```

## Primitive Data Types

| Data Type | Example        | Size    | Range                                 |
| --------- | -------------- | ------- | ------------------------------------- |
| `double`  | `0.0`          | 8 bytes | around 10<sup>308</sup> (decimals)    |
| `float`   | `0.0f`, `0.0F` | 4 bytes | around 10<sup>38</sup>  (decimals)    |
| `long`    | `0L`           | 8 bytes | around 10<sup>18</sup> (whole number) |
| `int`     | `0`            | 4 bytes | around 10<sup>9</sup> (whole number)  |
| `short`   | `0`            | 2 bytes | around 10<sup>4</sup> (whole number)  |
| `byte`    | `0`            | 1 byte  | around 100 (whole number)             |
| `char`    | `'A'`          | 2 bytes | (whole number)                        |

### Type Changing

#### Automatic Conversion (Promotion)

From smaller type to larger type.

> ```java
> double x = 7;
> ```
>
> `x` will be `7.0.`

#### Type Cast

From larger type to smaller type.

> ```java
> int y = (int)2.5;
> ```
>
> `y` will be `2`.

#### Mixed Arithmetic

> ```java
> int x = 3;
> double y = x/2;
> double z = x/2.0;
> ```
>
> `y` will be `1.0`:
>
> ​	`x/2` is `int` divided by `int`, so it will generate `2` (`int`), then converted to `2.0` (`double`).
>
> `z` will be `1.5`:
>
> ​	`x/2.0` is `int` divided by `int`, so `x` will be converted to `3.0` (`double`) first. Then `3.0/2.0` is `double` divided by `double`, generating `1.5`.
>
> `x` will still be `3` (`int`).

### ASCII Encoding

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1b/ASCII-Table-wide.svg/2560px-ASCII-Table-wide.svg.png" alt="File:ASCII-Table-wide.svg - Wikipedia" style="zoom:50%;" />

> ```java
> char ch = 'A';
> System.out.print(ch + ", " + (int)ch + ", ");
> ch += 1;
> System.out.print(ch + ", " + (int)ch);
> ```
>
> Output:
>
> ```
> A, 65, B, 66
> ```

> ```java
> char ch = 65;
> ```
>
> Is equivalent to:
>
> ```java
> char ch = 'A';
> ```

## Variables

A location in memory that stores data.

Variables have name, type (never change), and value.

Variables are first declared and then initialized.

### Declare

Specify name and type.

> ```java
> int x;
> ```

Do not declare one variable twice.

### Initialize

Assign value.

> ```java
> x = 2;
> ```

We can declare and initialize a variable simultaneously:

> ```java
> int x = 2;
> ```

We can assign one value to multiple variables:

> ```java
> int i = j = k = 1;
> ```

### Assignment Operation

```java
lvalue = rvalue;
```

`lvalue`: Must be evaluated to a memory location.

`rvalue`: Can be an expression or value.

The value at `lvalue`'s location is changed to `ravlue`.

> ```java
> int first = 20;
> int second = first;
> ```
>
> `first`: [20]	`second`: [20]
>
> You cannot do:
>
> ```java
> 20 = first;
> ```

## Console IO

### Output

```java
System.out.print(myVar);
```

Prints the value of `myVar` to the user’s console. However, it won’t end the line, so any other print statements will occur on the same line.

```java
System.out.println(myVar)
```

Prints the value of `myVar` and goes to the next line.

> ```java
> System.out.print(“hell”);
> System.out.println(“o”);
> System.out.println(“worl”);
> System.out.print(“d”);
> ```
>
> Output:
>
> ```
> hello
> worl
> d
> ```

### Input

We use `Scanner` to read in data.

`nextInt()`, `nextDouble()`,`next()`: Read in data.

`hasNext()`, `hasNextInt()`, `hasNextDouble()`: Check if there is still data to be read.

`useDelimiter(String)`: Read in data based on a formatting, e.g. `csv` file.

> ```java
> import java.util.*;
> public class Input{
>     public static void main(String args[]){
>       	Scanner keyboard = new Scanner(System.in); // Create a Scanner object.
>       	int value;
>         value = keyboard.nextInt();
>       	System.out.println("You entered " + value);
> 		}
> }
> ```

## Conditional Statements

`if`:

```java
if (condition) {
    // if (true) part
}
```

`if-else`:

```java
if (condition) {
    // if (true) part
}
else {
    // else (false) part
}
```

### Relational Operators

Used in an expression evaluated to a `boolean` value of `true` or `false`.

`<`: Less than.

`<=`: Less than or equal to. (No space in between.)

`>`: Greater than.

`>=`: Greater than or equal to.

`==`: Equal to.

​	`left == right`: Does `left` has the same value as `right`?

​	`lef = right`: Assign the value of `right` to `left`.

`!=`: Not equal to.

### `boolean` Data Type

Can hold the value `true` or `false`.

