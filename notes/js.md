# This are my notes about JS
***
# Variables

Variable allows **repeated** access to **values**

## How to Name Variables:

- **<u>P</u>ascal<u>C</u>ase**: used for **Types** and **Classes**.
- **DB_PASSWORD**: used for values **known before the launch** of an app/program and are **unchangable**.
- **camel<u>C</u>ase**: used for **variables**

Variable names should be **understandable**. (Bad examples: ~~foo, bar, test, xyz~~)

## Type system

**Static** - Variable type is determined in code with **_keywords_** and **is checked by compiler**. Languages that use Static typing: **C++, C, Java**

**Dynamic** - Variable type is determined by its **_value_** in the **moment of code execution**. Languages that use Dynamic typing: **JS, Python**

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

- **Initializing** (``let a``): permitted only for modifiable variables.
- **Initializing and assigning** (``const c=10``): the only way to initialize a constant variable. If tried to use only **initializing**, it will throw a SyntaxError: Missing initializer in const declaration.

# Objects

Objects can be:

- Sets of properties "Name: Value"
