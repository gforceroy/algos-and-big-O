# Intro to Algorithm Complexity & Big O Notation

## Overview
This lesson covers the basics of Big O notation.

There are two components to this lesson:
1. Lecture
2. In-Class Exercise: [Analyzing Algorithms](Big-O-Exercises.md)

## Learning Objectives
By the end of this lesson, you'll be able to:
- Explain how Big O notation is used to describe algorithms.
- Analyze algorithms to determine their Big O runtime.

## Prerequisites
* None

## Duration
1 hour total:
* 0.3 hour lecture
* 0.4 hour exercise 
* 0.3 hour review

## Why Big O Notation is Important?
![reasons](https://image.slidesharecdn.com/9-bigonotation-150305170945-conversion-gate01/95/9-big-onotation-11-638.jpg?cb=1425597049)

There are many ways to write the same program. 
One focus is mastering Algorithm Complexity and Big O Notation. 
What we want to do with this knowledge is to improve the performance of a software application. This is why it's important to understand which algorithm to use, depending upon the problem at hand.

### First is is important to know what a `computer algorithm` is. 
A `computer algorithm` is a series of steps the machine takes in order to take an input and compute an output. There are several ways to measure its performance. One of the metrics used to compare algorithms is using this notion of algorithm complexity.

Algorithms are basically functions.

Functions that are algorithms:

1. take in arguments

2. explicitly return values

#### 1.1 Example of an algorithm

Algorithm that counts the number of vowels in a word and returns the count:

```js
function countVowels(word) {
    var vowels = ['a', 'i', 'e', 'o', 'u'];
    var count = 0;
		for (var i = 0; i < word.length; i++) {
        for (var j = 0; j < vowels.length; j++) {
            if (word[i] === vowels[j]) {
                count++;
            }
        }
    }
    return count;
}

```

Algorithm complexity can be further divided into two types: time complexity and space complexity. Let's briefly touch on these two:

The time complexity, as the name suggests, refers to the time taken by the algorithm to complete its execution.
The space complexity refers to the memory occupied by the algorithm. In this lecture we will focus on time complexity. 

## What is Big O? 

![Big O chart](https://www.freecodecamp.org/news/content/images/2021/06/1_KfZYFUT2OKfjekJlCeYvuQ.jpeg)

Big O is short for Big O Notation.

Big O is how programmers talk about scalability of algorithms.

An algorithm's Big O Notation is determined by how long the algorithm takes to return output in the **worst case scenario**.

It offers you an approximation of how the software will respond in response to being “scaled” to address major (more complicated) issues.


## Some Examples of Big O Notation?

### Example 1:- O(1)
```
function sumNumbers(n1, n2) {
  console.log(n1 + n2)
}

```

In the first line function (sumNumbers) contains two input values (n1 and n2), and the number of operations (just one operation is included in the function body) does not change, therefore the run-time does not rely on the input. So not matter what this algo will go through one unit of work.

The "complexity" of this function is `O(1)`.


### Example 2:- O(n)

```
function loggingNumbers(n) {
  for (let i = 1; i <= n; i++) {
    console.log(n)
  }
}

function loggingNumbers2(n) {
  for (let i = 0; i < n; i++) {
    console.log(n)
  }

  for (let i = 0; i < n; i++) {
    console.log(n)
  }
}
```

O(n) specifies an algorithm which increases its performance directly and linearly in relation to the input size. The complexity of times rises as the size rises and at the same rate grows.

The "complexity" of `loggingNumbers` and `loggingNumbers2` is `O(n)`.

This means that it's a linear graph.

The first loggingNumbers method uses an argument, and the log is controlling how much iterations the loop will run. The loop depends upon that argument. If we transmit 5, we’ll get numbers from 1 to 5, if we send 10, we’ll get numbers from 1 to 10, and so on. Because the output is connected to the input, this approach expands linearly – O (n).

In the second loggingNumbers2 method, with two loops running one after the other (they are not nested). Therefore, one runs at n, another runs at n, so the last run is O (2n). Or is it? Or is it that? Again the equation may be simplified, the constant removed, and merely O(n) may be used as runtime.

### Example 3:- O(n^2)

```
function multiplicationTable(n) {
  for (let i = 0; i <= n; i++) {
    for (let j = 0; j <= n; j++) {
      console.log(i * j);
    }
  }
}
```
The "complexity" of `multiplicationTable` is `O(n^2)`.

There are two methods in the multiplicationTable for loops, each is iterated over n, which means that n * n is total. O(n2) is the time to run. The execution time of the nested loops equals the number of loops that are nested, if we had 3 loops the execution time was O(n3). And so forth. And so forth. Check the following visualization charts to show how much curve the runtime is at if the runtime is quadratic or cubic, such that the runtime grows with increasing the input, thereby reducing the efficiency of the procedure.


## Comparison of O(1), O(n), O(n^2)

Notice that the further right of the horizontal axis (x axis) you go, the vertical axis (y axis) goes up fastest for `O(n^2)`, slower for `O(n)` and constant for `O(1)`.

This means that `O(n^2)` runs slower than `O(n)`, which runs slower than `O(1)`.

![runtime_comparison.png](https://github.com/pavankat/big-o-in-plain-english/blob/master/runtime_comparison.png?raw=true)

## Conclusion
Algorithm complexity is used to measure the performance of an algorithm in terms of time taken and the space consumed.

Big(O) notation is one of the most commonly used metrics for measuring algorithm complexity. In this article you saw how to find different types of time and space complexities of algorithms using Big(O) notation. You'll now be better equipped to make trade-off decisions based on complexity in the future.




## Additional Resources
- [The Big O Cheat Sheet](http://bigocheatsheet.com/) is the authority on Big O complexities.
