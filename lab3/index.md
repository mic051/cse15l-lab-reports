# Lab 3

# Part 1

Failure inducing input:
`  @Test 
  public void testReverseInPlaceBad() {
    int[] input1 = { 1, 2, 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3, 2, 1 }, input1);
  }
`


Non-failure inducing input:
`
@Test 
    public void testReverseInPlace() {
      int[] input1 = { };
      ArrayExamples.reverseInPlace(input1);
      assertArrayEquals(new int[]{ }, input1);
    }
`
