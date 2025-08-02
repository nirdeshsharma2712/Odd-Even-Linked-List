# 📊 LeetCode Problem: Odd Even Linked List

## 🧩 Problem Statement

Given the head of a **singly linked list**, group all the nodes with **odd indices** together followed by the nodes with **even indices**, and return the reordered list.
The first node is considered **odd**, and the second node is **even**, and so on.
Note that the **relative order** inside both the even and odd groups should remain as it was in the **input**.



> **Note :**
> - You must solve the problem in O(1) extra space complexity and O(n) time complexity.



## 🧠 Approach: Two-Pointer Technique


- Initialize an empty string result to store the **final merged output**.

- Set **two pointers,** `i` and `j`, at the start of the two input strings `word1` and `word2`.

- **Traverse** both strings simultaneously using a loop:

- While both `i < word1.length()` and `j < word2.length()`:

> Append `word1[i]` and `word2[j]` to result.<br>

>  Increment both `i` and `j`.<br>

- Handle **remaining characters**:

> If `word1` has extra characters, append the remaining part starting from `i`.<br>

> If `word2` has extra characters, append the remaining part starting from `j`.

- Return the result string.



## ✅ Example Walkthrough

### Example 1

##### Input: head = [1,2,3,4,5]
##### Output: [1,3,5,2,4]

##### Explanation: 
<pre> The merged string will be merged as so:
  
  word1:  a   b   c
  word2:    p   q   r
  merged: a p b q c r
  
</pre>

### Example 2

##### Input: head = [2,1,3,5,6,4,7]
##### Output: [2,3,6,7,1,5,4]

##### Explanation: 
<pre> Notice that as word2 is longer, "rs" is appended to the end.
  
  word1:  a   b 
  word2:    p   q   r   s
  merged: a p b q   r   s
  
</pre>

### Example 3

##### Input: word1 = "abcd", word2 = "pq"
##### Output: "apbqcd"

##### Explanation: 
<pre> Notice that as word1 is longer, "cd" is appended to the end.
  
  word1:  a   b   c   d
  word2:    p   q 
  merged: a p b q c   d
  
</pre>

## 🛠️ Constraints

- The number of `nodes` in the **linked list** is in the range `[0, 10^4]`
- -10^6 <= Node.val <= 10^6
