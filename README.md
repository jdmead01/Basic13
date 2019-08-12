# Assignment: Basic 13

Write these as static functions callable from Program.cs.

```javascript 
public static void PrintNumbers()
{
    // Print all of the integers from 1 to 255.
}
public static void PrintTo255()
        {
            for (int i = 1; i < 256; i++)
            {
                Console.WriteLine(i);
            }
        }
```
**Print odd numbers between 1-255**
```javascript 
public static void PrintOdds()
{
    // Print all of the odd integers from 1 to 255.
}
public static void PrintOddTo255()
        {
            for (int i = 1; i < 256; i++)
            {
                if (i % 2 == 1) { Console.WriteLine(i); }

            }
        }
```
**Print Sum**
```javascript
public static void PrintSum()
{
    // Print all of the numbers from 0 to 255, 
    // but this time, also print the sum as you go. 
    // For example, your output should be something like this:
    
    // New number: 0 Sum: 0
    // New number: 1 Sum: 1
    // New Number: 2 Sum: 3
}
 public static void PrintSum()
        {
            int sum = 0;
            for (int i = 1; i < 256; i++)
            {
                sum += i;
                Console.WriteLine(sum);
            }
        }
```
**Iterating through an Array**
```javascript
public static void LoopArray(int[] numbers)
{
    // Write a function that would iterate through each item of the given integer array and 
    // print each value to the console. 
}
public static void PrintArray(params int[] vals)
        {
            foreach (var val in vals)
            {
                Console.WriteLine(val);
            }
        }
```
***Find Max***
```javascript
public static int FindMax(int[] numbers)
{
    // Write a function that takes an integer array and prints and returns the maximum value in the array. 
    // Your program should also work with a given array that has all negative numbers (e.g. [-3, -5, -7]), 
    // or even a mix of positive numbers, negative numbers and zero.
}
public static void FindMax(params int[] maxNums)
        {
            int max = maxNums[0];
            foreach (var maxNum in maxNums)
            {
                if (maxNum > max)
                {
                    max = maxNum;
                }
            }
            Console.WriteLine("Max: " + max);
        }
```
***Get Average***
```javascript
public static void GetAverage(int[] numbers)
{
    // Write a function that takes an integer array and prints the AVERAGE of the values in the array.
    // For example, with an array [2, 10, 3], your program should write 5 to the console.
}
public static void GetAvg(params int[] nums)
        {
            int sum = 0;
            foreach (var num in nums)
            {
                sum += num;
            }
            Console.WriteLine("avg: " + (sum / (nums.Length)));
        }
```
***Array With Odd Numbers***
```javascript
public static int[] OddArray()
{
    // Write a function that creates, and then returns, an array that contains all the odd numbers between 1 to 255. 
    // When the program is done, this array should have the values of [1, 3, 5, 7, ... 255].
}
public static void OddArray()
        {
            var y = new List<int>();
            for (int i = 1; i < 256; i++)
            {
                if (i % 2 == 1)
                {
                    y.Add(i);
                }
            }

            Console.WriteLine("array y: ");
            foreach (var i in y)
            {
                Console.Write( + i +", ");
            }
        }
```
***Greater Than Y***
```javascript
public static int GreaterThanY(int[] numbers, int y)
{
    // Write a function that takes an integer array, and a integer "y" and returns the number of array values 
    // That are greater than the "y" value. 
    // For example, if array = [1, 3, 5, 7] and y = 3. Your function should return 2 
    // (since there are two values in the array that are greater than 3).
}
public static void GtY(int y, params int[] compVals)
        {
            int count = 0;
            foreach (var compVal in compVals)
            {
                if (compVal > y)
                {
                    count++;
                }
                
            }
            Console.WriteLine($"Num on Ints greater than {y}: {count}");
        }
```
***Square the Values***
```javascript
public static void SquareArrayValues(int[] numbers)
{
    // Write a function that takes an integer array "numbers", and then multiplies each value by itself.
    // For example, [1,5,10,-10] should become [1,25,100,100]
}
public static void SquareVals(params int[] x)
        {
            for (int i = 0; i < x.Length; i++)
            {
                x[i] = x[i] * x[i];
            }

            Console.Write("Squared Vals: ");
            foreach (var val in x)
            {
                Console.Write(val + ", ");
            }
            Console.WriteLine("");
        }
```
***Eliminate Negative Numbers***
```javascript
public static void EliminateNegatives(int[] numbers)
{
    // Given an integer array "numbers", say [1, 5, 10, -2], create a function that replaces any negative number with the value of 0. 
    // When the program is done, "numbers" should have no negative values, say [1, 5, 10, 0].
}
public static void NoNegs(params int[] x)
        {
            for (int i = 0; i < x.Length; i++)
            {
                if (x[i] < 0)
                {
                    x[i] = 0;
                }
            }
```
***Min, Max, and Average***
```javascript
public static void MinMaxAverage(int[] numbers)
{
    // Given an integer array, say [1, 5, 10, -2], create a function that prints the maximum number in the array, 
    // the minimum value in the array, and the average of the values in the array.
}
public static void MinMaxAvg(params int[] x)
        {
            FindMax(x);
            GetAvg(x);
            int min = x[0];
            for (int i = 1; i < x.Length; i++)
            {
                if (x[i] < min)
                {
                    min = x[i];
                }
            }
            Console.WriteLine("min: " + min);
        }
```
***Shifting the values in an array***
```javascript
public static void ShiftValues(int[] numbers)
{
    // Given an integer array, say [1, 5, 10, 7, -2], 
    // Write a function that shifts each number by one to the front and adds '0' to the end. 
    // For example, when the program is done, if the array [1, 5, 10, 7, -2] is passed to the function, 
    // it should become [5, 10, 7, -2, 0].
}
public static void ShiftArray(List<int> shifties)
        {
            shifties.RemoveAt(0);
            shifties.Add(0);
            Console.Write("[ ");
            foreach (var shifty in shifties)
            {
                Console.Write(shifty + ", ");
            }
            Console.WriteLine("]");
        }
```
***Number to String***
```javascript
public static object[] NumToString(int[] numbers)
{
    // Write a function that takes an integer array and returns an object array 
    // that replaces any negative number with the string 'Dojo'.
    // For example, if array "numbers" is initially [-1, -3, 2] 
    // your function should return an array with values ['Dojo', 'Dojo', 2].
}
public static void NegToString(List<object> junk)
        {
            for (int i = 0; i < junk.Count; i++)
            {
                if ((int)junk[i] < 0)
                {
                    junk[i] = "Dojo";
                }
            }
            foreach (var item in junk)
            {
                Console.Write(item);
            }

            Console.WriteLine();
        }
```

