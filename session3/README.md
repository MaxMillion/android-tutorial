#Session 3: Creating a domain model

##Goal 

Learn how to build and test a plain Java project.

##Task

In this session you start by implementing the core game engine. The basic features are: 

- Given a number n, generate a random sequence of colors (red, blue, green) of length *n*.
- The player has to enter the same colors in the correct order. 

As Android is not needed for implementing the game engine, you should implement it as a normal java library. This has the advantage that the game engine is not tied to Android and can be reused in desktop or server applications. Furthermore, tests run a lot faster as there are less dependencies to load.

###Steps

1. Add a new **Gradle module** (not Android!) named `lib` inside the project. 
1. Create new src folders `src/main/java` and `src/test/java`
1. Create a class `com.esrlabs.simonsays.Game` in `src/main/java`
1. Create a test `com.esrlabs.simonsays.GameTest` in `src/test/java` and make it fail
1. Run the test via from the command line via `$./gradlew test`
1. Run the test from the IDE by executing the gradle task
1. Implement the game engine

###Things to watch our for

- Don't start too complicated. What is the simplest usable API to solve our problem? Remember, we don't know yet what we are going to need...
- How do we test generating a random sequence? Do we need to test it?

###Tips & Tricks

A little JUnit primer:

```java
import static org.junit.Assert.*;
import static org.hamcrest.CoreMatchers.*;

public class MyTest {

  @Before
  public void setup(){
    // optional setup 
  }
  
  @Test
  public void myTest(){
    boolean myBool = true;
    assertTrue(myBool);
    assertFalse(!myBool);
    assertEquals(myBool, false);
    assertThat(myBool, is(true));
    assertThat(myBool, is(not(false)));
  }

}
```

[Go to Session 4](https://github.com/esrlabs/android-tutorial/tree/master/session4/README.md)
