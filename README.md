
# JavaDoc CheatSheet

## Introduction
The main goal is to make documentation that doesn't rely on specific ways things are done and is short and clear in its explanations. You can mention dependencies when necessary. Also, feel free to use HTML tags in the comments. Most of the tags are easy to understand.

## Sample JavaDoc Class
```java
/**
 * The main purpose of the class or interface.
 * 
 * <p>
 * Additional details and description if needed. HTML tags are allowed.
 * </p>
 * 
 * @author kauts@dview.io
 * @version v1.0
 * @since 2023-11-21
 */
public class MyClass {

    /**
     * Brief description of the method.
     * 
     * <p>
     * Additional details and considerations if needed. HTML tags are allowed.
     * </p>
     * 
     * @param img The image to be passed. Write keywords in {@code code} tag.
     * @return The image to be returned. Write keywords in {@code code} tag.
     * @throws IOException If I/O exception occurred. Write keywords in {@code code} tag.
     * @deprecated Since version v1.0. Deprecated-text (optional).
     * @see package.ClassA
     * @see URL
     * @see ImageObserver This is descriptive text
     * @since Follow format throughout document
     */
    public ReturnType myMethod(ParameterType parameterName) throws SomeException {
        // Method implementation
    }

    /**
     * Brief description of the field.
     */
    private FieldType myField;

    /**
     * Brief description of the constructor.
     * 
     * <p>
     * Additional details if needed. HTML tags are allowed.
     * </p>
     * 
     * @param parameterName Brief description of the parameter.
     */
    public MyClass(ParameterType parameterName) {
        // Constructor implementation
    }
}

```
## Features
### Maven Checkstyle Configuration: 
Ensure code quality during builds using Maven. [See how to Configure in your project](maven/README.md)
### IntelliJ IDEA Java Checkstyle Configuration: 
Enforce coding standards directly within your IDE.[See how to Configure in Intellij](intellij/README.md)






