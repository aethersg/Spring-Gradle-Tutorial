***This is a Tutorial to create a spring project with gradle.*** 

**Steps involved:**

1. Create a Simple app
2. Build it with Gradle

**What is needed ?**
1. About 15 minutes
2. An IDE or text editor
3. JDK 6 or later.

***Project Structure***

```
+-- src
    |-- main
        |--java
            |--hello
                  |-- HelloWorld.java
                  |-- Greater.java
```
**To Build the code please run the following command**

```
gradle clean build

BUILD SUCCESSFUL in 1s
6 actionable tasks: 6 executed

```
upon seeing "BUILD SUCCESSFUL" it means that it has been built successful.
 
**Build your project with Gradle Wrapper**

The Gradle Wrapper is the preferred way of starting a Gradle build. It consists of a batch script for Windows and a shell script for OS X and Linux. These scripts allow you to run a Gradle build without requiring that Gradle be installed on your system. This used to be something added to your build file, but it’s been folded into Gradle, so there is no longer any need. Instead, you simply use the following command.

```
gradle wrapper 
```

building with the wrapper run the following command

```
./gradlew build
```

**Running the code via the wrapper**
To make this code runnable, we can use gradle’s application plugin. Add this to your build.gradle file.
```
apply plugin: 'application'

mainClassName = 'hello.HelloWorld'
```
after which run this command
```
./gradlew run
```

the result which we will see is this. 

```
./gradlew run
:compileJava UP-TO-DATE
:processResources UP-TO-DATE
:classes UP-TO-DATE
:run
The current local time is: 16:09:04.750
Hello world!

BUILD SUCCESSFUL

Total time: 2.749 secs
```