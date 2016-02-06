<b>Assert.DoesNotThrow</b> verifies that the delegate provided as an argument 
does not throw an exception.

```C#
void Assert.DoesNotThrow( TestDelegate code );
void Assert.DoesNotThrow( TestDelegate code, 
                          string message, params object[] parms);
```

<h4>See also...</h4>
 * [[Assert.Throws]]
 * [[Throws Constraint]]