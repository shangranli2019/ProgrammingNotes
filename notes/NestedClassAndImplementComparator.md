Nested class and Implementing Comparator



Prefer static nested class over inner class

## Static Nested Class



> Note: A static nested class interacts with the instance members of its outer class (and other classes) just like any other top-level class. In effect, a static nested class is behaviorally a top-level class that has been nested in another top-level class for packaging convenience.



## Inner Class (non-static nested class)





OuterClass.this to get the instance of the outer class



|                                    | Static Nested Class                           | Inner Class (non-static nested class)         |
| ---------------------------------- | --------------------------------------------- | --------------------------------------------- |
| Lifecycle                          | Always                                        | As long as the instance of the outer class    |
| Access to other fields and methods | Only static fields/methods in the outer class | Both the static and non-static fields/methods |





#### A specifal kind: Anonymous Class



##### One step further: Lamda Expression

Sometimes we have a problem with anonymous class: if logic in your anonymous class is very simple, writing out a full-blown anonymous class can be cumbersome. That's where lamda expression kicks in. (Todo: Java expression and lamda expression in depth)

## Implementing Comparator

1. Top-level class

   The simpliest way to implement a comparator is by a top-level class within the same .java file. Be aware that there can only be at most one public class in a .java file.

2. Static nested class

   The second solution is nest a static class with the main class. Be aware that sementically, a comparator belongs to the main class, NOT a instance of the main class. Therefore, being static is appriopriote here.

3. Anonymous class

   If the comparator class will only be used once here, we can write a anonymous class.

4. Lamda expression

   We can convert a simple anomymous class into a lamda expression.

5. Comparator.comparing()： todo





References:

https://docs.oracle.com/javase/tutorial/java/javaOO/nested.html