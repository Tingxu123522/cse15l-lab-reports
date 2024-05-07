 # **lab3** 
 
## Part 1

*1. A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown).*


```ruby
import static org.junit.Assert.*;
import org.junit.*;

public class ArrayTests {
	@Test 
	public void testReverseInPlace() {
    int[] input1 = {1, 2, 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3, 2, 1 }, input1);
    }
}
```

*2. An input that doesn't induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown).*

```ruby
import static org.junit.Assert.*;
import org.junit.*;

public class ArrayTests {
   @Test
  public void testReverseInPlaceSuccess() {
      int[] input = {1, 2, 1};
      ArrayExamples.reverseInPlace(input);
      assertArrayEquals(new int[]{1, 2, 1}, input);
  }
}
```

*3. The symptom, as the output of running the two tests above (provide it as a screenshot -- one test should pass, one test should fail).*
![Image](lab4-1.png)


*4. The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown).*

**Before Code Change:**

```ruby
public class ArrayExamples {
    static void reverseInPlace(int[] arr) {
        for (int i = 0; i < arr.length; i += 1) {
            arr[i] = arr[arr.length - i - 1];
        }
    }
}
```

**After Code Change:**
```ruby
public class ArrayExamples {
    static void reverseInPlace(int[] arr) {
        for (int i = 0; i < arr.length / 2; i += 1) {
            int temp = arr[i];
            arr[i] = arr[arr.length - i - 1];
            arr[arr.length - i - 1] = temp;
        }
    }
}
```

Briefly describe (2-3 sentences) why the fix addresses the issue.
