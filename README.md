# software_design_patterns

#### Why Patterns ?
Why do we need patterns? The blunt answer is we don't want to reinvent the wheel! Problems that occur frequently enough in tech life usually have well-defined solutions, which are flexible, modular and more understandable. These solutions when abstracted away from the tactical details become design patterns.


### Example
Let's consider an example to understand what design patterns are and how do they get applied. The class constructor is one of the basic concepts in an object orientated language. The constructors help create objects of the class and can take in parameters. Let us take the following class as an example.

```

public class Aircraft {

    private String type;

    public Aircraft(String type) {
        this.type = type;
    }
}

In the above example, we have the default constructor for the class that takes in a 
single parameter the type of the aircraft. Now say after a few days, you realize you want to add 
additional properties to your Aircraft class. 
Say you want to add the color of the aircraft as a property, but you have already released a 
version of your library and can't modify the original constructor. The solution is to add another
constructor with two parameters like so


public class Aircraft {

    private String type;
    private String color;

    public Aircraft(String type) {
        this.type = type;
    }

    public Aircraft(String type, String color) {
        this.type = type;
        this.color = color;
    }
}

If you continue this way you'll end up having a bunch of constructors with increasing number of arguments looking like a telescope:


Aircraft(String type)
Aircraft(String type, String color)
Aircraft(String type, String color, String prop3)
Aircraft(String type, String color, String prop3, String prop4)  
  
```
The telescoping pattern is called an anti-pattern: how NOT to do things! The way to approach a class with an increasing number of variables is to use the Builder Pattern that we'll discuss in depth in the following chapters.

Seasoned developers are expected to be well-versed in design patterns and applying them makes the code reusable and maintainable for future. Design patterns aren't limited to object orientated languages but also exist for other domains of Computer Science such as distributed systems, big data system or user interface.'


https://medium.com/@modestofiguereo/design-patterns-2-the-builder-pattern-and-the-telescoping-constructor-anti-pattern-60a33de7522e

https://stackify.com/solid-design-open-closed-principle/



