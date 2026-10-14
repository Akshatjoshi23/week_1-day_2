# Week 1, Day 2: Java HashMap Practice

A small set of Java exercises exploring how `HashMap` stores and retrieves data, and how key equality affects lookups.

## What This Covers

- Creating and using `HashMap` key-value pairs
- Adding, retrieving, replacing, and counting entries
- Comparing object identity with logical equality
- Implementing `equals()` and `hashCode()` for custom keys
- Looking up a value with a different but equivalent key object
- Observing how hash collisions are handled
- Using immutable fields in objects used as map keys

## Examples

| File | Focus |
| --- | --- |
| `hashmap.java` | Uses student objects as keys, demonstrates equal keys replacing an entry, looks up a key with a new object, and shows colliding integer keys. |
| `hashMapEquals.java` | Compares student objects using their ID and checks the matching hash codes. In this example, names do not affect equality. |

## Run the Examples

Install a JDK and open a terminal in this directory. Compile and run either example:

```bash
javac hashmap.java
java hashmap
```

```bash
javac hashMapEquals.java
java hashMapEquals
```

The class names are case-sensitive. Each example is self-contained and can be compiled separately.

## Key Takeaway

For a custom class used as a `HashMap` key, `equals()` and `hashCode()` must agree: objects that are equal must return the same hash code. The examples show that `HashMap` uses this behavior to find equivalent keys, even when they are different object instances.