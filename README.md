Download Link: https://assignmentchef.com/product/solved-cs2310-assignment-2-dices
<br>
In this assignment, you are going to write a C++ program to find out the probability of different total values when several unbiased dices were thrown at the same time. The program makes use of various techniques including basic I/O, arithmetic, conditional control structures, loops and arrays.

<strong><u>Problem Statement:</u></strong>

It is well known that a dice is a cube with number 1 to 6 written on each face, but in fact there exist irregular dices with different number of faces (e.g. 4, 5, 8…etc). A coin can also be considered as a dice of 2 faces as well.

When an unbiased dice is thrown, the probability of having different face value should be equal. For instance, a typical cubic dice should give a probability of 1/6 for the face values 1,2,3,4,5 and 6.

If two cubic dices were thrown, the total of the face values on the two dices is in range [2..12]. However, the probability of each “total value” is not equal. For example, the total of 4 is having a probability of 3/36 (for combinations 1+3, 2+2 and 3+3) while the probability of a total of 2 is only 1/36 (when both dices give 1).

In this assignment, you need to write a program to find out the probability of each “total value” when several unbiased irregular dices <em>(possibly with different number of faces)</em> are thrown at the same time.

The program should first read in the number of dices, <strong>N</strong> (range: [1..12] inclusive).

Then the program will read in N numbers, each representing the number of faces of a dice (range: [1..12] inclusive. Of course it’s physically impossible to have a one-face dice, but you can imagine that it’s a dice with 1 written on all faces)

Finally the program should output the probability of each “total value” in fractional form. <em>(you may assume that the denominator of the fraction is always small enough for a 32bit integer)</em>

<strong> </strong>

<strong><u>Grading:</u></strong>

This assignment is divided into 2 parts: The (easier) part 1 containing only the basic features and the (harder) part 2 with extra requirements. The two parts carry equal weighting.




Submission of non-compilable code (non-cpp files) or having an output format which differs from the specification will result in zero marks. The markers will make no manual effort in modifying your code and make it compilable. It is suggested that you test your program on PASS with VS2017 first before final submission.

<h1>Part 1 – Basic part</h1>

<ul>

 <li>You may assume that all input numbers are valid.</li>

 <li>Print in ascending order of the “total value”.</li>

 <li>The “total value” is right aligned to the field width of the largest number.</li>

 <li>No simplification of fraction is needed.</li>

 <li>Default PASS runtime limit (5 sec) is adopted for each test case.</li>

</ul>




<h2>Sample input/output (content typed by the user is highlighted in yellow)</h2>

<strong> </strong>

Input the number of dice(s): 2

Input the number of faces for the 1st dice: 6

Input the number of faces for the 2nd dice: 6

Probability of  2 = 1/36

Probability of  3 = 2/36

Probability of  4 = 3/36        Largest total value is 12 (width=2),

Probability of  5 = 4/36 therefore 2 is padded with a leading

Probability of  6 = 5/36

Probability of  7 = 6/36        space.

Probability of  8 = 5/36

Probability of  9 = 4/36

Probability of 10 = 3/36

Probability of 11 = 2/36

Probability of 12 = 1/36




Input the number of dice(s): 5

Input the number of faces for the 1st dice: 1

Input the number of faces for the 2nd dice: 2

Input the number of faces for the 3rd dice: 3

Input the number of faces for the 4th dice: 4

Input the number of faces for the 5th dice: 5

Probability of  5 = 1/120

Probability of  6 = 4/120

Probability of  7 = 9/120

Probability of  8 = 15/120         Don’t forget the appropriate ordinal

Probability of  9 = 20/120         suffix (i.e.  st / nd / rd / th)

Probability of 10 = 22/120

Probability of 11 = 20/120

Probability of 12 = 15/120

Probability of 13 = 9/120

Probability of 14 = 4/120

Probability of 15 = 1/120




Input the number of dice(s): 9

Input the number of faces for the 1st dice: 1

Input the number of faces for the 2nd dice: 1

Input the number of faces for the 3rd dice: 1

Input the number of faces for the 4th dice: 1

Input the number of faces for the 5th dice: 1

Input the number of faces for the 6th dice: 1

Input the number of faces for the 7th dice: 1

Input the number of faces for the 8th dice: 1

Input the number of faces for the 9th dice: 1

Probability of 9 = 1/1




<h1>Part 2 – Enhanced part</h1>

<ul>

 <li>It is guaranteed that the user input are numbers, however it may not be an integer in range [1..12]. Upon invalid input, the program should print the error message and keep reading until a valid number is entered.</li>

</ul>

<em>(Apart from that, no other error checking is needed)</em>

<ul>

 <li>The output should be sorted in descending order of probability. If there are several “total values” having the same probability, print in ascending order of “total”.</li>

 <li>The fraction should be in the simplest form (e.g. 1/2 instead of 6/12).</li>

 <li>Runtime limit is 1 second for each test case.</li>

</ul>

<strong> </strong>

<h2>Sample input/output (content typed by the user is highlighted in yellow)</h2>




Input the number of dice(s): 2

Input the number of faces for the 1st dice: 6

Input the number of faces for the 2nd dice: 6

Probability of  7 = 1/6

Probability of  6 = 5/36          7 is having the highest probability, so

Probability of  8 = 5/36          printed first. 6/36 is simplified to 1/6.

Probability of  5 = 1/9

Probability of  9 = 1/9

Probability of  4 = 1/12

Probability of 10 = 1/12        Both 4 &amp; 10 have the same probability,

Probability of  3 = 1/18        but since 4&lt;10, so 4 is printed first.

Probability of 11 = 1/18

Probability of  2 = 1/36

Probability of 12 = 1/36




<table width="0">

 <tbody>

  <tr>

   <td width="574">Input the number of dice(s): 2Input the number of faces for the 1st dice: 6Input the number of faces for the 2nd dice: 0Error: input value should be integer in range 1..12Input the number of faces for the 2nd dice: 14Error: input value should be integer in range 1..12Input the number of faces for the 2nd dice: 5.5Error: input value should be integer in range 1..12Input the number of faces for the 2nd dice: 6Probability of  7 = 1/6Probability of  6 = 5/36Probability of  8 = 5/36Probability of  5 = 1/9Probability of  9 = 1/9Probability of  4 = 1/12Probability of 10 = 1/12Probability of  3 = 1/18Probability of 11 = 1/18Probability of  2 = 1/36 Probability of 12 = 1/36</td>

  </tr>

 </tbody>

</table>


