# CSE11 Introduction to Programming and Computational Problem-Solving

## Introduction

*Ex.* `Foo.java`:

```java
public class Foo {
  public static void main( String[] args ) {
    System.out.println(“Hello world”);
} }
```

`Foo` is class name (capitalized first letter).

### Compile

Translate human-readable Java language program into an equivalent program in a language closer to what the computer can understand.

```shell
$ javac Foo.java
```

Generate `Foo.class` file (binary).

### Run

Use Java applications (with a `main()` method).

```shell
$ java Foo
```

Can use shortcut to combine compile and run, but not recommended:

```shell
$ java Foo.java
```

## Primitive Data Types

| Data Type | Ex.    | Size    | Range                        |
| --------- | ------ | ------- | ---------------------------- |
| `double`  | `0.0`  | 8 bytes | around 10^308^ (decimals)    |
| `float`   | `0.0f` | 4 bytes | around 10^38^  (decimals)    |
| `long`    | `0L`   | 8 bytes | around 10^18^ (whole number) |
| `int`     | `0`    | 4 bytes | around 10^9^ (whole number)  |
| `short`   | `0`    | 2 bytes | around 10^4^ (whole number)  |
| `byte`    | `0`    | 1 byte  | around 100 (whole number)    |
| `char`    | `'A'`  | 2 bytes | (whole number)               |

Type changing:

- Automatic conversion (promotion): from smaller type to larger type.

  - *Ex.*

    ```java
    double x = 7;
    ```

- Type cast: from larger type to smaller type.
