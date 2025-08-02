# 📊 LeetCode Problem: Odd Even Linked List

## 🧩 Problem Statement

Given the head of a **singly linked list**, group all the nodes with **odd indices** together followed by the nodes with **even indices**, and return the reordered list.
The first node is considered **odd**, and the second node is **even**, and so on.

> **Note :**
> - Note that the **relative order** inside both the even and odd groups should remain as it was in the **input**.
> - You must solve the problem in O(1) extra space complexity and O(n) time complexity.



## 🧠 Approach: Two-Pointer Technique

- Initialize two pointers:

> - One for the **odd-indexed** `nodes`
> - One for the **even-indexed** `nodes`, and keep track of the **even list head.**

- Traverse using:

> - `odd->next = even->next`, then move `odd` forward.
> - `even->next = odd->next`, then move `even` forward.

- Continue until end of **list**.

Finally, link the last odd node to the `head` of **even list** to complete the rearrangement.



## ✅ Example Walkthrough

### Example 1

##### Input: head = [1,2,3,4,5]
##### Output: [1,3,5,2,4]


### Example 2

##### Input: head = [2,1,3,5,6,4,7]
##### Output: [2,3,6,7,1,5,4]



## 🛠️ Constraints

- The number of `nodes` in the **linked list** is in the range `[0, 10^4]`
- -10^6 <= Node.val <= 10^6
