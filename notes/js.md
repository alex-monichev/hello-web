# These are my notes about JS

***

# Variables

Variable allows **repeated** access to **values**

## How to Name Variables

- **<u>P</u>ascal<u>C</u>ase**: used for **Types** and **Classes**.
- **DB_PASSWORD**: used for values **known before the launch** of an app/program and are **unchangable**.
- **camel<u>C</u>ase**: used for **variables**

Variable names should be **understandable**. (Bad examples: ~~foo, bar, test, xyz~~)

## Type system

- **Static** - Variable type is determined in code with **_keywords_** and **is checked by compiler**. Languages that use Static typing: **C++, C, Java**

- **Dynamic** - Variable type is determined by its **_value_** in the **moment of code execution**. Languages that use Dynamic typing: **JS, Python**

## Object Types

### Primitive Types

These types are stored **directly in the variable** and hold their actual values. When you assign a primitive type to a variable, it contains the value itself. If you copy a primitive value to another variable, you create a separate copy.

These types are:

- String
- Boolean
- Number
- Null
- Undefined
- Symbol

### Reference Types

These types are stored **as references to their values**. When you assign a reference type to a variable, the variable holds a reference (or a pointer) to the location in memory where the value is stored. If you **_copy_** a reference type to another variable, **both variables point to the same object in memory**.

These types are:

- Object
- Array
- Function

## Variable initializing

- **let**: Modifiable
- **const**: Constant
- **var**: Modifiable, **depracated, not used**

There's two ways to initialize a variable:

- **Initializing** (`let a`): permitted only for modifiable variables.
- **Initializing and assigning** (`const c=10`): the only way to initialize a constant variable. If tried to use only **initializing**, it will throw a SyntaxError: Missing initializer in const declaration.

***

# Objects

In JavaScript, Objects are a _fundamental data structure_ and a key part of the language. Objects are used to represent complex data structures. They can be **used for everything** from simple data containers to more complex entities (like functions, arrays, and even custom types).

## Objects can be

- ### Collections of key-value pairs

Objects are collections of **key-value** pairs, where each key is a property name, and each value can be any data type (e.g., numbers, strings, functions, or even other objects). The **syntax** is: `propertyName: propertyValue`

- ### Almost all things in JS

In JavaScript, **_nearly everything_** that isn’t a primitive type is an object (e.g., arrays, functions, dates, and even errors). Objects are flexible and form the foundation of many JavaScript features.

- ### Reference Type variables

Objects are a type of reference variable. Unlike primitive data types, which store their values directly, objects store a reference to the location in memory where the data is kept. This means that when you assign or copy an object, you’re working with references to the same data.

## Object Creation

Object can be made through:

- ## Object Literal `{}`

The **simplest and most common way** to create an object is by using object literal syntax.

Syntax:

```js
let objectName = {
  property1: value1,
  property2: value2
};
```

- ## `new`

This approach is less common but useful if you’re **dynamically adding properties** after creating the object.

Syntax:

```js
let objectName = new Object();
```

##

There're more ways to make an Object, but these are most common in JS.

> Order of elements in an Object doesn't matter

## Accessing Object Properties

In JavaScript, you can access and interact with an object's properties using two main syntaxes: **Dot Notation** and **Bracket Notation**. Each has its own use cases and advantages.

### Dot Notation

Dot Notation is the simpler and more common way to access properties. It's **straightforward and visually cleaner**, making code easy to read.

**Pros**:

- Dot notation is best when you know the **exact name of the property** and it follows standard variable naming rules (e.g., it doesn’t start with a number and **contains no spaces or special characters**).

- It’s generally preferred **when you have control over the property names** because it’s more _concise_ and _readable_.

**Cons**:

Dot notation cannot be used if:

- The property name contains spaces (`person["first name"]`).
- The property name starts with a number (`person["123name"]`).
- The property name is stored in a variable and not known ahead of time.

### Bracket Notation

Bracket Notation is more versatile, allowing you to access properties using dynamic expressions or property names that **don’t follow standard naming conventions**.

**Pros**:

- Bracket notation is flexible and **allows access to properties with names that contain spaces, special characters, or numbers** (e.g., `person["first name"]` or `person["123name"]`).
- It is ideal for **dynamic property access**, where the property name might be stored in a variable or created at runtime.
- Useful when iterating over an object's properties with a loop, especially if property names are not known ahead of time.

**Cons**:

- Bracket notation can be **less concise and readable** than dot notation, especially when accessing simple properties.
- It’s **more prone to errors if the property name in quotes is misspelled**, as there’s **no auto-completion support in many editors**.
- Requires **explicit quotation marks** around property names, which can sometimes make the code look cluttered.

### Resumé

| Feature | Dot Notation | Bracket Notation |
| :- | :-: | :-: |
| Simple Syntax | Yes | No |
| Dynamic Access | No | Yes |
| Special Characters | No | Yes |
| Variable Properties | No | Yes |

***