# unmeta
This is a fork from [oliver-jonas/unmeta](https://github.com/oliver-jonas/unmeta)

An Android Gradle plugin to remove all Kotlin @DebugMetadata annotations from the build output.

Kotlin @DebugMetadata annotations are not fully processed by ProGuard / R8 and contain un-obfuscated symbol information, both in binary and plain text forms. This information can be used to more easily reverse engineer your code.

This plugin allows removing all Kotlin @DebugMetadata annotations from generated class files. 

In the Gradle build log you will see one line for each class where the plugin removed the metadata annotation:

```
Removed @DebugMetadata annotation from .../MainActivity.class
```
