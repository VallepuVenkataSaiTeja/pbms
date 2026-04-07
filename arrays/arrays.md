Here are some **commonly asked array questions in JavaScript interviews**, ranging from basic to advanced, with a mix of concepts and coding challenges:

---

## 🔹 Basic Array Questions

1. **What is an array in JavaScript?**
2. Difference between:

   * `map()` vs `forEach()`
   * `filter()` vs `find()`
3. How do you:

   * Add/remove elements (`push`, `pop`, `shift`, `unshift`)?
4. What does `slice()` vs `splice()` do?
5. How to check if a variable is an array?

---

## 🔹 Intermediate Coding Questions

### 1. Reverse an Array

```js
function reverseArray(arr) {
  return arr.reverse();
}
```

---

### 2. Find Maximum Number in Array

```js
function maxNum(arr) {
  return Math.max(...arr);
}
```

---

### 3. Remove Duplicates

```js
function removeDuplicates(arr) {
  return [...new Set(arr)];
}
```

---

### 4. Flatten an Array

```js
function flatten(arr) {
  return arr.flat(Infinity);
}
```

---

### 5. Find Second Largest Number

```js
function secondLargest(arr) {
  let unique = [...new Set(arr)];
  unique.sort((a, b) => b - a);
  return unique[1];
}
```

---

## 🔹 Advanced Questions

### 6. Two Sum Problem

```js
function twoSum(arr, target) {
  let map = new Map();

  for (let i = 0; i < arr.length; i++) {
    let diff = target - arr[i];
    if (map.has(diff)) {
      return [map.get(diff), i];
    }
    map.set(arr[i], i);
  }
}
```

---

### 7. Group Anagrams

```js
function groupAnagrams(words) {
  let map = {};

  for (let word of words) {
    let key = word.split('').sort().join('');
    if (!map[key]) map[key] = [];
    map[key].push(word);
  }

  return Object.values(map);
}
```

---

### 8. Rotate Array

```js
function rotate(arr, k) {
  k = k % arr.length;
  return [...arr.slice(-k), ...arr.slice(0, -k)];
}
```

---

### 9. Find Missing Number (0 to n)

```js
function missingNumber(arr, n) {
  let total = (n * (n + 1)) / 2;
  let sum = arr.reduce((a, b) => a + b, 0);
  return total - sum;
}
```

---

### 10. Kadane’s Algorithm (Max Subarray Sum)

```js
function maxSubArray(arr) {
  let max = arr[0];
  let current = arr[0];

  for (let i = 1; i < arr.length; i++) {
    current = Math.max(arr[i], current + arr[i]);
    max = Math.max(max, current);
  }

  return max;
}
```

---

## 🔹 Tricky / Frequently Asked

* Merge two sorted arrays
* Move all zeros to end
* Find intersection of two arrays
* Chunk array into groups
* Sort without using `sort()`
* Find majority element
* Longest consecutive sequence

---

## 🔹 Conceptual Questions

* How arrays are stored internally in JS?
* Difference between arrays and objects
* What are sparse arrays?
* What is array destructuring?
* What is immutability in arrays?

---

Here are **important Array conceptual questions** specifically asked in **service-based interviews** (like TCS, Infosys, Wipro, Accenture):

---

# 🧠 Array Conceptual Questions (Very Important)

## 🔹 Basics

### 1. What is an array in JavaScript?

👉 An array is a special object used to store multiple values in a single variable.

---

### 2. How are arrays different from objects?

* Arrays → ordered, index-based
* Objects → key-value pairs

---

### 3. Are arrays in JavaScript fixed or dynamic?

👉 Dynamic (size can grow/shrink)

---

### 4. How do you check if a variable is an array?

```js
Array.isArray(arr)
```

---

### 5. What are sparse arrays?

👉 Arrays with missing indexes
Example:

```js
let arr = [1, , 3]; // empty slot
```

---

## 🔹 Important Methods (Very Frequently Asked)

### 6. Difference between `map()` and `forEach()`

* `map()` → returns new array
* `forEach()` → does not return

---

### 7. Difference between `filter()` and `find()`

* `filter()` → returns all matching elements
* `find()` → returns first match

---

### 8. Difference between `slice()` and `splice()`

* `slice()` → non-destructive (returns new array)
* `splice()` → modifies original array

---

### 9. What does `reduce()` do?

👉 Reduces array to a single value

---

### 10. What is the use of `includes()`?

👉 Checks if value exists in array

---

## 🔹 Memory & Behavior

### 11. Are arrays stored by value or reference?

👉 Reference

```js
let a = [1,2];
let b = a;
b.push(3);
// both change
```

---

### 12. What is shallow copy vs deep copy?

* Shallow → copies reference (nested objects shared)
* Deep → full independent copy

---

### 13. How to clone an array?

```js
let copy = [...arr];
```

---

### 14. What happens when you use `const` with arrays?

👉 You can modify elements, but cannot reassign the array.

---

## 🔹 Advanced Concepts (Sometimes Asked)

### 15. What is array destructuring?

```js
let [a, b] = [1, 2];
```

---

### 16. What is the time complexity of common operations?

| Operation       | Complexity |
| --------------- | ---------- |
| Access by index | O(1)       |
| Insert at end   | O(1)       |
| Insert at start | O(n)       |
| Search          | O(n)       |

---

### 17. What is the difference between `push()` and `unshift()`?

* `push()` → adds at end
* `unshift()` → adds at beginning

---

### 18. Can arrays have different data types?

👉 Yes (JavaScript is loosely typed)

```js
[1, "hello", true]
```

---

### 19. What is length property in arrays?

👉 Returns number of elements (highest index + 1)

---

### 20. What happens if you set `length` manually?

```js
arr.length = 2;
```

👉 Array gets truncated

---

# 🎯 Pro Tip (Very Important)

In service-based interviews:

* They often mix **1 conceptual + 1 coding question**
* If you explain concepts clearly → high chance of selection

---

Got it 👍 — for **service-based companies** (like TCS, Infosys, Wipro, Accenture, Cognizant), the focus is usually **simpler logic + basics + clean coding**, not very hard algorithms.

Here are the **Top Array Questions commonly asked in service-based interviews** 👇

---

# ✅ Top Array Questions (Service-Based Level)

## 🟢 Very Important Basics

### 1. Reverse an Array

👉 Iterative or using built-in

---

### 2. Find Largest & Smallest Element

👉 Basic loop logic

---

### 3. Sort an Array

👉 Using `sort()` + custom comparator

---

### 4. Second Largest Element

👉 Without sorting (preferred)

---

### 5. Remove Duplicates

👉 Using `Set` or loop

---

## 🟡 Frequently Asked Logic Questions

### 6. Move All Zeros to End

```js
Input: [0,1,0,3,12]
Output: [1,3,12,0,0]
```

---

### 7. Count Even and Odd Numbers

👉 Simple traversal

---

### 8. Find Sum and Average of Array

---

### 9. Merge Two Arrays

---

### 10. Find Missing Number

👉 From 1 to N

---

## 🟠 Slightly Tricky (But Common)

### 11. Find Duplicate Number

👉 Using Set or nested loop

---

### 12. Find Intersection of Two Arrays

---

### 13. Rotate Array by 1 Position

---

### 14. Frequency of Elements

👉 Count occurrences

---

### 15. Check if Array is Sorted

---

## 🔵 Occasionally Asked (Good to Know)

### 16. Two Sum (basic version)

---

### 17. Find All Pairs with Given Sum

---

### 18. Leader Elements in Array

👉 Elements greater than all right-side elements

---

### 19. Maximum Difference (j > i)

---

### 20. Kadane’s Algorithm (sometimes asked)

---

# 🎯 What Interviewers Expect

In service-based companies, they check:

* Basic **logic building**
* Clean and readable code
* Knowledge of **loops & conditions**
* Some **built-in methods**
* Ability to explain your approach

👉 They usually **DON’T expect advanced DS/Algo like FAANG**

---

# 💡 Preparation Strategy (Important)

Focus on:

* Arrays + Strings (MOST important)
* Basic sorting
* Simple problem solving
* Writing code without errors

---

Here are the **Top 20 most asked Array questions in FAANG JavaScript interviews**, carefully selected based on real interview trends (Amazon, Google, Meta, Apple, Netflix):

---

# 🔥 Top 20 Array Interview Questions (FAANG Level)

## 🟢 Easy → Foundation Builders

### 1. Two Sum

Find indices of two numbers that add up to a target.

---

### 2. Best Time to Buy and Sell Stock

Maximize profit from stock prices.

---

### 3. Contains Duplicate

Check if array has any duplicates.

---

### 4. Maximum Subarray (Kadane’s Algorithm)

Find contiguous subarray with largest sum.

---

### 5. Move Zeroes

Move all `0`s to the end without changing order.

---

## 🟡 Medium → Core Problem Solving

### 6. Product of Array Except Self

Return array where each element = product of others.

---

### 7. Container With Most Water

Find max water container using two pointers.

---

### 8. 3Sum

Find all unique triplets that sum to 0.

---

### 9. Rotate Array

Rotate array by `k` steps.

---

### 10. Find Minimum in Rotated Sorted Array

Binary search based tricky question.

---

### 11. Search in Rotated Sorted Array

Modified binary search.

---

### 12. Merge Intervals

Merge overlapping intervals.

---

### 13. Insert Interval

Insert and merge interval.

---

### 14. Subarray Sum Equals K

Count subarrays with sum = k (prefix sum + hashmap).

---

## 🔴 Hard → FAANG Favorites

### 15. Trapping Rain Water

Calculate trapped water using two pointers.

---

### 16. Sliding Window Maximum

Use deque for O(n) solution.

---

### 17. Minimum Window Substring

Classic sliding window problem.

---

### 18. Longest Consecutive Sequence

Use set for O(n) solution.

---

### 19. First Missing Positive

Find smallest missing positive integer.

---

### 20. Median of Two Sorted Arrays

Binary search + partition logic (very common in Google).

---

# 💡 Important Patterns Behind These Questions

Instead of memorizing, focus on patterns:

* **Two Pointers** → 3Sum, Container, Trapping Rain Water
* **Sliding Window** → Substring, max window
* **Prefix Sum** → Subarray sum
* **Hashing** → Two Sum, duplicates
* **Binary Search** → Rotated arrays, median
* **Greedy** → Stock problems
* **Stack/Deque** → Sliding window max

---

# 🚀 Pro Tip

In FAANG interviews, they care more about:

* Approach clarity
* Time/space complexity
* Edge cases
* Communication

Not just code.

---

