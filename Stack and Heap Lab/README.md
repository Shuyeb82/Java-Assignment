# Java Lab: Stack and Heap Memory

This repository contains two Java programs demonstrating how Java manages objects, instance variables, local variables, and method calls using stack and heap memory.

## Files

| File | Problem |
|---|---|
| `StackHeapDemo.java` | Problem 1: Stack and Heap memory with a `Student` class |
| `EmployeeMemoryDemo.java` | Problem 2: Stack frames, heap objects, and a local inner class |

---

## Problem 1: `StackHeapDemo.java`

### Description

- Defines a `Student` class with the instance variable `age`.
- Uses the `display()` method with the local variable `marks`.
- Creates a `Student` object in the `main()` method.
- Prints the object's identity hash code using `System.identityHashCode()`.

**Source Code:** [StackHeapDemo.java](https://github.com/Shuyeb82/Java-Assignment/blob/main/Stack%20and%20Heap%20Lab/StackHeapDemo.java)

### Sample Input

```text
Age: 20
Marks: 85
```

### Sample Output

```text
Student Object Created
Object Identity Hash Code: 1072591677
Instance Variable (age): 20
Local Variable (marks): 85
```

---

## Problem 2: `EmployeeMemoryDemo.java`

### Description

- Defines an `Employee` class with the instance variable `salary`.
- Uses the `display()` method with the local variable `bonus`.
- Defines a local inner class named `Report` inside the `display()` method.
- The `Report` class contains a `show()` method.
- Prints the identity hash codes of both the `Employee` and `Report` objects.

### Sample Input

```text
Enter salary: 30000
Enter bonus: 5000
```

### Sample Output

```text
Employee Object Created
Employee Identity Hash Code: 1072591677

Inside display() Method:
Salary (Instance Variable): 30000
Bonus (Local Variable): 5000

Report Object Created
Report Identity Hash Code: 1421795058
Report: Employee salary is 30000

Memory Concept:
Employee object -> Heap
Report object -> Heap
salary -> Instance field
bonus -> Local variable in display()
show() -> Executes in its own method frame
```

**Note:** The identity hash code may differ between program executions. It is not the actual memory address of an object.

---

## Memory Concepts

| Item | Stored In |
|---|---|
| Objects (`new Student()`, `new Employee()`, `new Report()`) | Heap |
| Instance variables (`age`, `salary`) | Heap, as part of their respective objects |
| Local variables (`marks`, `bonus`) | Stack frame, conceptually |
| Local object references (`s`, `e`, `r`) | Typically in the method's stack frame, conceptually |
| Method calls (`main()`, `display()`, `show()`) | Each active method call has its own stack frame |

**Important:** These descriptions represent the usual conceptual model of Java memory management. JVM implementation details may vary.

---

## How to Run

### Requirements

- Java Development Kit (JDK) 8 or later
- Command Prompt or Terminal

### Problem 1: StackHeapDemo.java

Compile the program:

```bash
javac StackHeapDemo.java
```

Run the program:

```bash
java StackHeapDemo
```

### Problem 2: EmployeeMemoryDemo.java

Compile the program:

```bash
javac EmployeeMemoryDemo.java
```

Run the program:

```bash
java EmployeeMemoryDemo
```

---

## Conclusion

These programs demonstrate the basic concepts of Java stack and heap memory, including object creation, instance variables, local variables, object references, method stack frames, and local inner classes.

They help illustrate how Java manages memory during program execution.
