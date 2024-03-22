```java
    public static boolean equals(final Object a, final Object b) {
        if (a == null && b == null) {
            return true;
        } else if (a == null || b == null) {
            return false;
        }
        return a.equals(b);
    }
```
## Tests to achieve predicate coverage
``` java
import org.junit.Test;
import static org.junit.Assert.*;

public class EqualsTest {

    @Test
    public void testBothObjectsNull() {
        Object a = null;
        Object b = null;
        boolean result = Equals.equals(a, b);
        assertTrue(result);
    }

    @Test
    public void testOneObjectNull() {
        Object a = "test";
        Object b = null;
        boolean result = Equals.equals(a, b);
        assertFalse(result);
    }

    @Test
    public void testBothObjectsNonNullAndEqual() {
        Object a = "test";
        Object b = "test";
        boolean result = Equals.equals(a, b);
        assertTrue(result);
    }

    @Test
    public void testBothObjectsNonNullAndNotEqual() {
        Object a = "test";
        Object b = "different";
        boolean result = Equals.equals(a, b);
        assertFalse(result);
    }

    @Test
    public void testBothObjectsAreTheSameNonNullObject() {
        Object a = obj;
        Object b = obj;
        boolean result = Equals.equals(a, b);
        assertTrue(result);
    }

    @Test
    public void testBothObjectsAreDifferentTypes() {
        Object a = "test";
        Object b = 123;
        boolean result = Equals.equals(a, b);
        assertFalse(result);
    }
}
```

## Tests to achieve clause coverage
``` java
import org.junit.Test;
import static org.junit.Assert.*;

public class EqualsTest {

    @Test
    public void testBothObjectsNull() {
        Object a = null;
        Object b = null;
        boolean result = Equals.equals(a, b);
        assertTrue(result);
    }

    @Test
    public void testOneObjectNullAndOtherNonNull() {
        Object a = "test";
        Object b = null;
        boolean result = Equals.equals(a, b);
        assertFalse(result);
  }

    @Test
    public void testOneObjectNullAndOtherNonNull2() 
        a = null;
        b = "test";
        result = Equals.equals(a, b);
        assertFalse(result);
    }

    @Test
    public void testBothObjectsNonNullAndEqual() {
        Object a = "test";
        Object b = "test";
        boolean result = Equals.equals(a, b);
        assertTrue(result);
    }

    @Test
    public void testBothObjectsNonNullAndNotEqual() {
        Object a = "test";
        Object b = "different";
        boolean result = Equals.equals(a, b);
        assertFalse(result);
    }

    @Test
    public void testBothObjectsAreTheSameNonNullObject() {
        Object obj = "test";
        Object a = obj;
        Object b = obj;
        boolean result = Equals.equals(a, b);
        assertTrue(result);
    }

    @Test
    public void testBothObjectsAreDifferentTypes() {
        Object a = "test";
        Object b = 123;
        boolean result = Equals.equals(a, b);
        assertFalse(result);
    }
}
```

## Tests to achieve CACC
``` java
import org.junit.Test;
import static org.junit.Assert.*;

public class EqualsTest {

    @Test
    public void testBothObjectsNull() {
        Object a = null;
        Object b = null;
        boolean result = Equals.equals(a, b);
        assertTrue(result);
    }

    @Test
    public void testOneObjectNullAndOtherNonNull() {
        Object a = "test";
        Object b = null;
        boolean result = Equals.equals(a, b);
        assertFalse(result);
  }

    public void testOneObjectNullAndOtherNonNull2(){
        a = null;
        b = "test";
        result = Equals.equals(a, b);
        assertFalse(result);
    }

    @Test
    public void testBothObjectsNonNullAndEqual() {
        Object a = "test";
        Object b = "test";
        boolean result = Equals.equals(a, b);
        assertTrue(result);
    }

    @Test
    public void testBothObjectsNonNullAndNotEqual() {
        Object a = "test";
        Object b = "different";
        boolean result = Equals.equals(a, b);
        assertFalse(result);
    }

    @Test
    public void testBothObjectsAreTheSameNonNullObject() {
        Object obj = "test";
        Object a = obj;
        Object b = obj;
        boolean result = Equals.equals(a, b);
        assertTrue(result);
    }

    @Test
    public void testBothObjectsAreDifferentTypes() {
        Object a = "test";
        Object b = 123;
        boolean result = Equals.equals(a, b);
        assertFalse(result);
    }
}
```
## Tests to achieve RACC
``` java
import org.junit.Test;
import static org.junit.Assert.*;

public class EqualsTest {

    @Test
    public void testBothObjectsNull() {
        Object a = null;
        Object b = null;
        boolean result = Equals.equals(a, b);
        assertTrue(result);
    }

    @Test
    public void testOneObjectNullAndOtherNonNull() {
        Object a = "test";
        Object b = null;
        boolean result = Equals.equals(a, b);
        assertFalse(result);
    }

    public void testOneObjectNullAndOtherNonNull2() {
        a = null;
        b = "test";
        result = Equals.equals(a, b);
        assertFalse(result);
    }

    @Test
    public void testBothObjectsNonNullAndEqual() {
        Object a = "test";
        Object b = "test";
        boolean result = Equals.equals(a, b);
        assertTrue(result);
    }

    @Test
    public void testBothObjectsNonNullAndNotEqual() {
        Object a = "test";
        Object b = "different";
        boolean result = Equals.equals(a, b);
        assertFalse(result);
    }

    @Test
    public void testBothObjectsAreTheSameNonNullObject() {
        Object a = obj;
        Object b = obj;
        boolean result = Equals.equals(a, b);
        assertTrue(result);
    }

    @Test
    public void testBothObjectsAreDifferentTypes() {
        Object a = "test";
        Object b = 123;
        boolean result = Equals.equals(a, b);
        assertFalse(result);
    }
}
```


