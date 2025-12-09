# Homework C Practice Instructions

Often in the software engineering industry, you will be asked to pickup a new language on the fly. This is because a language is a tool, and you are often needing to select the best tool for the job. In this course, we use C as it helps us better understand the underlying system that we are working with. Learning a new language can be challenging, but the best way to is to find relationships to what you know while also taking time to practice the syntax differences. This homework is designed to help you learn a new language, and get you comfortable with the process of learning a new language. You will be asked to learn the basics of C, and then implement a few functions in C. You will also be asked to write a few tests in C. 

- [Homework C Practice Instructions](#homework-c-practice-instructions)
  - [Learning Objectives](#learning-objectives)
  - [Provided Files](#provided-files)
  - [Write your Code and Tests](#write-your-code-and-tests)
    - [Compiling Your Code](#compiling-your-code)
      - [:star: Compile Frequently :star:](#star-compile-frequently-star)
    - [Report.md](#reportmd)
  - [📝 Grading Rubric](#-grading-rubric)
    - [Submission Reminder 🚨](#submission-reminder-)
  - [📚 Resources](#-resources)

## Learning Objectives

The learning objects for this assignment are
* Practice basic C syntax for structures both on the stack and heap
* Practice with C arrays
* Practice with C strings
* Practice with Structs

## Provided Files
👉🏽 **Task** 👈🏽: look through provided files to see what is going on while also updating the comments at the top of the file. Make sure to ask questions if you are unsure what is going on!

For this assignment (and all others) you will be provided some files to work with. It is always best to look through the provided files to see what is going on while also updating the comments at the top of the file. 

The files provided for this assignment are:
* [cpractice.h](../src/cpractice.h) - This files contains all the functions you need to implement along with the structs you need to use. You will notice the function signatures are provided, along with the struct definitions. You will need to implement the functions in [cpractice.h](../src/cpractice.h) following the comments provided. The various print functions are intentionally implemented for you, so you can use them. This is called a header library, and is still valid C code. 
* [main.c](../src/main.c) - This file contains a sample run of the program testing the various features. You can run this file to see the output of the program, but it is recommended you wait until the end to run it. 
* [tests.c](../src/tests.c) - This file will be where you will store your tests. **FOR EVERY FUNCTION** you implement except for free'ing memory, you will immediately want to implement a few tests to ensure it is working properly. These tests should try to break the function / look at edge cases, in addition to just making sure works. In true test driven development, you should actually write the tests first, before writing a function. Take a look at this code, how are we running the functions (notice we are adding them to the array).
   > A key concept here - write tests after *every* function. Don't wait until the end. You will thank yourself if you incrementally write tests as you go.


## Write your Code and Tests
👉🏽 **Task** 👈🏽: Write your functions!

Now following the comments in [cpractice.h](../src/cpractice.h), implement the functions. You will also need to write tests for each function in [tests.c](../src/tests.c). 

:star: **Important** :star:  
You should incrementally write your code, testing as you go along! 


### Compiling Your Code
As a guideline, here are steps to compile your code via the command line. Even if you are using an IDE, you may find it is easier to compile via the command line.

1. Open your terminal and navigate to the directory with your .h and .c files. 
   * Reminder, you can use `cd` to change directories, and `ls` to list the files in the current directory.
2. To compile run:
   * `gcc -Wall tests.c -o test.out` - and then to run your tests, run `./test.out`.
   * `gcc -Wall main.c -o main.out` - and then to run your program, run `./main.out`. 


> [!IMPORTANT]  
> You should always compile with the `-Wall` flag. This will show you all warnings, which are often errors in your code. You should always fix all warnings before submitting your code as we compile with the -Wall flag on the grading server.

#### :star: Compile Frequently :star:  
It is very easy to have a small error in your code (missing a semicolon), and then have a ton of errors when you compile. It is best to compile frequently, so you can catch these errors early. Often professional developers will compile after every 'chunk' (often 3-4 lines) of code they write. This is a good habit to get into. While the code may not be fully working, it helps you catch errors early. This is also why you should test every function *as you write them*. 

### Report.md 
You will notice there are questions in your [readme.md](../README.md) and [Report.md](../Report.md) file. You will want to answer these questions. For this course, we will be doing a lot with Markdown files, so it is important to get used to them. You may even want to review the [Markdown Guide](https://guides.github.com/features/mastering-markdown/) to get a better understanding of how to format your readme.md file.

Every assignment will have to fill out both a README.md and Report.md, so make sure you review them!

> [!IMPORTANT]
> A common mistake in markdown files is not viewing how they render on the website. Always go to github and review
> how the markdown files really look. Graders go to github to review the code even though you submit on gradescope,
> as it will properly render latex math (which is required for a lot of reports). 


## 🤖 Use of LLMs
For this assignment, you should **not use LLMs for the main source code, or for your report**. For your report, it is VERY important to reason through the answers! Make sure you understand, and resubmissions will help you clarify understanding. 

For the main source code, you are learning C, and as such, it is important to really think through the memory model. However, you are also to the point of starting to co-create with AI, so you are welcome to use AI to help you build your test functions. 

**Reminder**: Every function that doesn't contain print statements (all the ones you wrote in your main implementation) should have a series of test cases written in `tests.c`.

### Why Use LLMs for Testing?
Writing comprehensive test cases is a skill that AI can help accelerate. By learning to write clear specifications and descriptions of what you expect, you're developing skills in:
- **Precise communication** - describing exact behavior and edge cases
- **Test-driven thinking** - thinking about pre/postconditions before implementation
- **Validation** - checking that generated tests match your understanding

### Method 1: Code Completion (e.g., GitHub Copilot)

If you have code completion enabled, creating a very clear comment is essential. The quality of your comment directly impacts the quality of the generated test.

**Example of a good test case comment:**
```c 
/**
 * Test case for reverse_array(arr, size).
 * Passing in the array [1, 2, 3, 4, 5, 6]
 * modifies the `arr` array by reversing the values
 * causing arr to be [6, 5, 4, 3, 2, 1]. 
 * Size matches the range to reverse. Simple case. 
 * precondition: arr = [1, 2, 3, 4, 5, 6], size = 6
 * postcondition: arr = [6, 5, 4, 3, 2, 1], size = 6
 * return 1 if test passed, 0 if test failed. 
 **/
void test_reverse_array_simple() {
    // Let copilot generate the implementation
}
```

**Key elements of a good test comment:**
1. **Function being tested** - What function is this testing?
2. **Input description** - What specific input are you providing?
3. **Expected behavior** - What should happen?
4. **Preconditions** - State of the system/data before the test
5. **Postconditions** - Expected state after the test runs
6. **Test category** - Is this a simple case, edge case, error case?

**Important workflow:**
- Write the comment FIRST (this proves you understand what should happen)
- Let the AI generate the test implementation
- **Add the test to your test suite in main() immediately**
- **Run it before moving on** - Never generate multiple tests without running them
- If it fails, debug whether your understanding was wrong or the generated code is incorrect

### Method 2: Prompt-Based Systems (e.g., Claude, ChatGPT)

#### Generating Individual Test Cases

Use this prompt structure to generate a specific test case:

````
Generate a simple test case for the following function:

```c 
/**
 * Reverses an array *in place* (meaning you don't copy into another array)
 * 
 * For example, if the array is [1, 2, 3, 4, 5] then the array should be
 * [5, 4, 3, 2, 1]
 * 
 */
void reverse_array(int *arr, int size)
```

Requirements for the test case:
1. Include clear comments explaining what is being tested
2. Show the precondition (initial array state)
3. Show the postcondition (expected array state after reversal)
4. Follow C syntax and best practices
6. Return 1 if the test passes or 0 if it fails. 
7. Make sure to print the item being tested as the start of the test.  

After generating the test case, explain:
- Why this is a correct test case
- What aspect of the function it validates
- Any potential issues or edge cases it doesn't cover
````

**Why the "explain after" is important:**
- It forces you to understand WHY the test is correct
- It helps you identify gaps in test coverage
- It builds your mental model of testing strategies

#### Discovering Edge Cases

Use this prompt to explore what you should test:

````
Given the following function definition, what are common test cases and edge cases you recommend I check?

```c 
/**
 * Reverses an array *in place* (meaning you don't copy into another array)
 * 
 * For example, if the array is [1, 2, 3, 4, 5] then the array should be
 * [5, 4, 3, 2, 1]
 * 
 */
void reverse_array(int *arr, int size)
```

For each test case you suggest:
1. Explain what aspect it tests (normal operation, boundary condition, error case, etc.)
2. Describe the expected behavior
3. Note any assumptions about how the function should handle edge cases

Organize your suggestions by category:
- Simple/Normal cases
- Boundary cases (empty arrays, single element, etc.)
- Edge cases (very large arrays, etc.)
- Potential error conditions

Do NOT write the actual test code yet - just describe what should be tested and why.
````

**Why ask for descriptions first:**
- You think through what SHOULD happen before seeing code
- You can discuss edge case behavior with instructors/TAs if unclear
- You learn to identify testing categories systematically

#### Generating Complete Test Suites

Once you understand what needs testing, use this prompt:

````
Based on our discussion of test cases for reverse_array(), generate a complete test suite in C.

Function to test:
```c 
void reverse_array(int *arr, int size)
```

Generate test functions for these categories:
1. Simple case - even-length array
2. Simple case - odd-length array  
3. Boundary case - empty array (size = 0)
4. Boundary case - single element
5. Boundary case - two elements
6. Tests should return 1 if they pass correctly or 0 if they fail.
7. Each test needs to print what is being tested at the start of the test. 

For each test function:
- Use descriptive function names (e.g., test_reverse_array_even_length)
- Include comments with preconditions and postconditions
- Make it easy to add to a main() test runner

I already have a main() test runner that I will be adding the tests into. 
````

### Best Practices for AI-Assisted Testing

1. **Always specify before generating**: Write comments describing what SHOULD happen before asking AI to generate the code
2. **Run tests incrementally**: Add and run one test at a time
3. **Verify your understanding**: If a test fails, make sure you understand why before fixing it
4. **Don't blindly trust generated code**: AI can make mistakes - review every test
5. **Use AI to explore edge cases**: Ask "what am I missing?" to find cases you didn't think of
6. **Document your thinking**: Add comments explaining WHY each test case matters

### What to Include in Your Submission

When submitting `tests.c`, include:
- **Test function names** that clearly describe what they test
- **Comments** explaining the precondition and postcondition for each test
- **A note** in comments if a test was AI-generated, and whether you modified it
- **A main() function** that runs all tests and reports results clearly

### Red Flags - When AI Usage Goes Wrong

❌ **Don't do this:**
- Generating 20 test cases without running any
- Copying test code you don't understand
- Using AI to write your main implementation functions
- Letting AI write your report or analysis

✅ **Do this:**
- Use AI to accelerate test case creation
- Verify every generated test yourself
- Learn from AI suggestions about edge cases
- Use AI as a teaching tool, not a replacement for thinking

### Additional Prompts for Better Results

**If the LLM needs more context about your testing framework:**
```
I'm writing tests in C without a formal testing framework. 

My tests should:
- Be individual void functions with descriptive names
- Use printf() to show test progress
- Either use assert() or manual if-checks to verify correctness
- return 1 if passed or 0 if ailed

Generate tests following this pattern.
```

**If you want to understand testing strategy better:**
```
I'm learning about software testing in C. Explain the difference between:
- Normal/happy path test cases
- Boundary conditions
- Edge cases
- Error conditions

For each category, give me 2-3 examples relevant to array manipulation functions in C.

Then quiz me: give me a function signature and ask me to identify what categories of tests I should write.
```

**If the generated test doesn't compile or work:**
```
The following test case you generated doesn't compile:

[paste the code]

The error I'm getting is: [paste error message]

Please:
1. Explain what's wrong
2. Explain the correct C syntax/approach
3. Provide the corrected version
4. Explain why the correction works
```


> [!IMPORTANT]  
> Remember: The goal is to learn C and develop good testing habits. AI is a tool to help you explore test cases and write tests faster, but you must understand every line of code in your submission.


## 📝 Grading Rubric

1. Learning (AG)
   * Code compiles with no warnings or errors
   * Swap works
   * Basic create fibonacci array works
   * Basic reverse array works
2. Approaching  (AG)
   * Works for edge cases for fibonacci array, and reverse array
   * double array works
   * Copy array works in simple cases (0 <= start < end < size)
   * Create point works
   * Create Polygon, rectangle, and triangle works
   * Copy array works in wrap cases (0 <= end < start < size)
   * Calculate area works for different shapes
3. Meets  (MG)
   * Report.md questions answered correctly up until the
     technical interview questions.
   * At least 2 references included using ACM format.
4. Exceeds  (MG)
   * At least 3 commits       
   * All values stored on the heap are properly freed
   * Complete test coverage in tests.c. Including multiple tests for every function except for the ones we provided (the ones that included print), and edge cases checked. You do not have to test free_polygon (but you should look it up in the debugger).
   * Code documented properly (including explaining tests)
   * Technical Interview question answered (at least one)
   * Leet/Coding Practice Problem(s) submitted (at least one)



### Submission Reminder 🚨
For manually graded elements, we only guarantee time to submit for a regrade **IF** you submit by the **DUE DATE**. Submitting late may mean it isn't possible for the MG to be graded before the **AVAILABLE BY DATE**, removing any windows for your to resubmit in time. While it will be graded, it is always best to *submit by the due date*, so you have full opportunity to improve your grade.


## 📚 Resources
* [Learning C](https://www.linkedin.com/learning/learning-c-5/)  is a tutorial on C in LinkedIn Learning (free with your Northeastern Login)
* [Essential C](https://www.linkedin.com/learning/c-essential-training/) is another tutorial on C in LinkedIn Learning (free with your Northeastern Login)
* [Learn C Interactive Tutorial](http://www.learn-c.org/)
* [clang compiler](https://clang.llvm.org/)
* [gcc compiler](https://www.gnu.org/software/gcc/)
