# CSE11 Introduction to Programming and Computational Problem-Solving

## Introduction

> `Foo.java`:
>
> ```java
> public class Foo {
>   public static void main( String[] args ) {
>     System.out.println(“Hello world”);
> 	}
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

| Data Type | Ex.    | Size    | Range                                 |
| --------- | ------ | ------- | ------------------------------------- |
| `double`  | `0.0`  | 8 bytes | around 10<sup>308</sup> (decimals)    |
| `float`   | `0.0f` | 4 bytes | around 10<sup>38</sup>  (decimals)    |
| `long`    | `0L`   | 8 bytes | around 10<sup>18</sup> (whole number) |
| `int`     | `0`    | 4 bytes | around 10<sup>9</sup> (whole number)  |
| `short`   | `0`    | 2 bytes | around 10<sup>4</sup> (whole number)  |
| `byte`    | `0`    | 1 byte  | around 100 (whole number)             |
| `char`    | `'A'`  | 2 bytes | (whole number)                        |

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

## Variables

