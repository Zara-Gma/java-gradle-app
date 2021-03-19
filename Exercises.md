# EXERCISE 1: Build jar artifact

You want to deploy the artifact to share that library with all team members. So:

    try to build the jar file

The Build will fail, because of a compile error in a test, so you can't build the jar.
./gradlew build

# EXERCISE 2: Run tests

    Fix the test, by changing "true" string to true boolean.
    Run gradle test to execute only the tests and check the fix.
./gradlew test

# EXERCISE 3: Clean and build App

You fixed the test. Now:

    clean the build folder with gradle clean and
    try to build jar file again.
./gradlew clean
./gradlew build

# EXERCISE 4: Start application
    Start the jar file to test that the application
    runs successfully as a jar file

java -jar build/libs/bootcamp-java-project-1.0-SNAPSHOT.jar


# EXERCISE 5: Start App with 2 Parameters

Now you want to add parameters to your application, so you and other users can pass different values on startup.

    Add parameter input to the Java code (see separate code snippet, which you can copy)
    Rebuild the jar file
    Execute the jar file again with 2 params


# Code snippet for Exercise 5! # Code snippet to add inside Application.java on line 16 Logger log = LoggerFactory.getLogger(Application.class); try { String one = args[0]; String two = args[1]; log.info("Application will start with the parameters {} and {}", one, two); } catch (Exception e) { log.info("No parameters provided"); } 

Java -jar Gradle param1 param2
