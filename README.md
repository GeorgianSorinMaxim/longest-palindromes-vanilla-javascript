# MAT Software Team Coding Challange #

### Task ###

Write an application that finds the 3 longest unique palindromes in a supplied string. For the 3 longest
palindromes, report the palindrome, start index and length, in descending order of length.

### Example Output ###

Given the input string: "sqrrqabccbatudefggfedvwhijkllkjihxymnnmzpop", the output should be:

```javascript
Text: hijkllkjih, Index: 23, Length: 10

Text: defggfed, Index: 13, Length: 8

Text: abccba, Index: 5 Length: 6
```

### Deliverables ###

-  Your solution may be submitted in a language of your choice.
-  Please include instructions for how to build and run your code.
-  Don't forget to include any tests in the package.

### Guidance ###

-  You shouldn't spend more than a couple of hours on the solution.
-  We expect candidates to create code that is production quality - the solution 
should be correct, reliable, maintainable, reusable, portable and efficient.
-  For further guidance see Clean Code: A Handbook of Agile Software  Craftsmanship by Robert C.Martin.

### Development ###

- This application is built using JavaScript.
- The solution is a O(N^2) time and O(1) space solution.
- A palindrome can be observed from its center, consequently there are 2N-1 such centers.
- Expanding a palindrome around its center takes O(N) time, hence the overall complexity is O(N^2).
- The 3 longest arrays are being saved in an array of objects that is sorted in a descending order by lenght.
- If the array contains more than 3 elements, then the shortest palindromes are being removed from the array.

### Assumption ###

-  A single character is not a palindrome.
-  The solution will only print the 3 longest unique palindromes in the supplied string. If the number of longest unique palindromes that the program can find is bigger than 3, then the program will not print the rest of the found palindromes.

### Execution ###

1. Download this repository.
2. `Unzip` the downloaded repository.
3. Open the unzipped directory.
4. Drag the `index.html` file in a browser client and open the Developer Tools:
	In Chrome right-click and choose Inspect.
	In Firefox right-click and choose Inspect Element.
	In Safari open the Developer TOools in the Advanced panel in the Preferences menu.

### Tests ###

-  A simple test function has been developed that tests if the result of the solution contains 3 elements, but it does not contain checks for the palindromes content.

### How to make the code more maintainable, reusable, portable and efficient ###

-  The function can be refractored by provinding a number input for allowing for the display a custom number of longest palindromes.