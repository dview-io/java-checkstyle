# IntelliJ IDEA Java Checkstyle Setup
![Add Code Style to IntelliJ.gif](gifs%2FAdd%20Code%20Style%20to%20IntelliJ.gif)
1. Clone this repo locally `git clone git@github.com:dview-io/dview-java-checkstyle.git`
2. In IntelliJ IDEA, Go to `Settings` > `Editor` > `Code Style` 
3. Click on Settings Icon in `Code Style` and then `Import Scheme` > `Import Intellij Code Style XML`
4. Select the intellij-java-dview-google-style.xml file browser window

## Setup IntelliJ for easy Class level JavaDoc generation

![IntelliJ automatic JavaDoc Generator.gif](gifs%2FIntelliJ%20automatic%20JavaDoc%20Generator.gif)
1. Open IntelliJ IDEA.
2. Go to File -> Settings (or IntelliJ IDEA -> Preferences on macOS).
3. In the Settings/Preferences window, navigate to `Editor` -> `File and Code Templates`.
4. Select Class and then add/edit
```
#if (${PACKAGE_NAME} && ${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end
/**
 * Description of the ${NAME} class.
 * <p>
 * Additional details if needed.
 * </p>
 *
 * @author kauts@dview.io
 * @version 1.0
 * @since ${YEAR}-${MONTH}-${DAY}
 */
#parse("File Header.java")
public class ${NAME} {
}
```
5. Select Interface and then edit/add
```
#if (${PACKAGE_NAME} && ${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end
/**
 * Description of the ${NAME} interface.
 * <p>
 * Additional details if needed.
 * </p>
 *
 * @author kauts@dview.io
 * @version 1.0
 * @since ${YEAR}-${MONTH}-${DAY}
 */
#parse("File Header.java")
public interface ${NAME} {
}
```
6. Select Enum and then edit/add
```
#if (${PACKAGE_NAME} && ${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end
/**
 * Description of the ${NAME} enum.
 * <p>
 * Additional details if needed.
 * </p>
 *
 * @author kauts@dview.io
 * @version 1.0
 * @since ${YEAR}-${MONTH}-${DAY}
 */
#parse("File Header.java")
public enum ${NAME} {
}
```