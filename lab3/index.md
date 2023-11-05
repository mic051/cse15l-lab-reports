# Lab 3

## Part 1

### Failure Inducing Input:

```
  @Test 

  public void testReverseInPlaceBad() {
  
    int[] input1 = { 1, 2, 3 };
    
    ArrayExamples.reverseInPlace(input1);
    
    assertArrayEquals(new int[]{ 3, 2, 1 }, input1);
    
  }
```

[!Image][Screenshot 2023-11-05 041144.png]

### Non-Failure Inducing Input:

```
    @Test

    public void testReverseInPlace() {

      int[] input1 = { };

      ArrayExamples.reverseInPlace(input1);

      assertArrayEquals(new int[]{ }, input1);

    }
```

[!Image][Screenshot 2023-11-05 041411.png]

### Bug (Before and After Fix)

```
static void reverseInPlaceBad(int[] arr) {

    for(int i = 0; i < arr.length; i += 1) {

      arr[i] = arr[arr.length - i - 1];

    }

  }
```

```
  static void reverseInPlace(int[] arr) 

  {

    for (int i = 0; i < arr.length / 2; i++) 

    {

      int temp = arr[i];

      arr[i] = arr[arr.length - i - 1];

      arr[arr.length - i - 1] = temp;

    }

  }
```

The bug within the code is that it doesn't swap the elements. The code only assigns the value on the left with the value on the right. This works only works for the first half of the array. For the second half of the array, it gains the values right, which has already been reassigned to the second half, resulting in no change for the second half. The fix changes how long the `for` loop runs and introduces an `int`. The `int` holds the value of the left so it doesn't get lost after getting reassigned. After the beginning part of the array is assigned, the latter part is given the value of the `int`, which is the value from the first half. Since both ends are being swapped at the same time, the `for` loop iterates for half of the length.

## Part 2


