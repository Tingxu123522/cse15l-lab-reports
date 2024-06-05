# Ting Xu's Lab Report 5

## Part 1 - Debugging Scenario

1.

![Image](lab9-1.jpg)

2. **Response from a TA:**

   Hello, It looks like the output `[1, 5, 2, 4, 3, 6]` is showing that the sorting algorithm isn't functioning as it should. This suggests that perhaps only the initial swap operation is taking place, rather than the whole array being sorted properly.

   In your ArrayProcessor.java, the sorting logic currently seems to execute just one pass through the array. A single pass typically only works if the array is already nearly sorted, which doesn't appear to be the case here.

   To address this, consider implementing a more comprehensive sorting algorithm. A simple Bubble Sort would be effective for learning purposes. This method requires multiple passes through the array, continuing until no further swaps are needed.

   I hope this helps solve your problem, if you have any other questions, please feel free to ask.

3. 

   


