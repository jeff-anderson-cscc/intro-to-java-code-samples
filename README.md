
## Classic Hello World
```.java
public class Main {

  public static void main (String[] args) {
    System.out.println("Hello world!");
  }

}
```

## Using Passed Parameters
```.java
public class Main {

  public static void main (String[] args) {
 
    System.out.println("Parameters passed:");

    for (String parameter : args) {
      System.out.println(parameter);
    }
  }

}
```


## Returning an Exit Code

```.java
public class Main {

  public static void main (String[] args) {
    int returnValue = 0;

    if (args.length == 1) {
      try {
        returnValue = Integer.parseInt(args[0]);
      }
      catch (NumberFormatException e) {
        System.out.println("You did not pass an integer value");
      }
    }
    System.out.println("Exiting with value: " + returnValue);
    System.exit(returnValue);
  }

}
```