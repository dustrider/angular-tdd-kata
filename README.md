## Angular TDD Kata

The following is a TDD Kata - an exercise in coding, refactoring and test-first, that you should apply daily for at least 15 minutes. The point is to progressively get better and faster over time, not to deliver something.

Start from scratch in each application, for the initial try we can keep it simple with a single input box and a single output label.

## Evaluation and Review

After the 15 minutes swap chairs with a peer and look at what they've done and their approach for 5 minutes and then get together as a group to discuss what worked and approaches for the remaining 10 minutes.

**Remember to strictly time box this activity.**

Bragging rights go to the person that got the farthest in the objectives that everyone agrees are properly tested.

## Before you start:

*   Try not to read ahead.
*   Do one task at a time. The trick is to learn to work incrementally.
*   Make sure you only test for **correct inputs**. there is no need to test for invalid inputs for this kata

## String Calculator

1.  Create a simple String calculator with a function **Add(numbers)**
    1.  The method can take a string with 0, 1 or 2 numbers, and will return their sum (for an empty string it will return 0) for example **“” or “1” or “1,2”**
    2.  Start with the simplest test case of an empty string and move to 1 and two numbers
    3.  Remember to solve things as simply as possible so that you force yourself to write tests you did not think about
    4.  Remember to refactor after each passing test
2.  Allow the Add method to handle an unknown amount of numbers
3.  Allow the Add method to handle new lines between numbers (instead of commas).
    1.  the following input is ok: “1\n2,3” (will equal 6)
    2.  the following input is NOT ok: “1,\n” (not need to prove it - just clarifying)
4.  **Support different delimiters**
    1.  to change a delimiter, the beginning of the string will contain a separate line that looks like this: “//[delimiter]\n[numbers…]” for example “//;\n1;2” should return three where the default delimiter is ‘;’ .
    2.  the first line is optional. all existing scenarios should still be supported
5.  Calling Add with a negative number will throw an exception “negatives not allowed” - and the negative that was passed.if there are multiple negatives, show all of them in the exception message
6.  Numbers bigger than 1000 should be ignored, so adding 2 + 1001 = 2
7.  Delimiters can be of any length with the following format: “//[delimiter]\\n” for example: “//[\*\*\*]\\n1\*\*\*2\*\*\*3” should return 6
8.  Allow multiple delimiters like this: “//[delim1][delim2]\\n” for example “//[\*][%]\\n1\*2%3” should return 6.
9.  make sure you can also handle multiple delimiters with length longer than one char
