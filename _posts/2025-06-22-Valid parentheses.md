---
title: " Valid parentheses "
date: 2025-06-22 00:00:00 +0000
categories: [leetcode problems]
tags: [algorithmes]
---

# let's get started 




first of all i needed to learn what a stack is in DSA's 
i found the following explanation very helpful : 




1. Stack Basics
LIFO Structure (Last In, First Out) like a pile of plates.

Key Operations:

push: Add to the top.

pop: Remove from the top.

peek: Check the top item.

isEmpty: Check if empty.





2. Valid Parentheses Problem : 

the goal is to check if a string of brackets ((), {}, []) has correctly nested and matched pairs.

Why a Stack?

Tracks the order of opening brackets to ensure correct closing (e.g., {[]} is valid; ([)] is not).

Counters fail because they only track quantity, not order.





3. Now into the valid Approach

first we initialize the empty stack.

we then loop through each character:

Opening bracket ((, {, [) will be Pushed onto the stack.

for the Closing bracket (), }, ]) we'll check : 

If the stack is empty → invalid.

otherwise we'll Pop the top of the stack and check for a matching pair.

Final Check: the Stack must be empty (all brackets closed correctly).





4. here is an Example to clarify the process : 


Valid: " ()[]{}  "

( → push, ) → pop ( matches () .

[ → push, ] → pop ( matches [)  .

{ → push, } → pop ( matches {)  .
→ Stack empty → valid.

Invalid: "([)]"

( → push, [ → push.

) → tries to pop [ ( mismatch with () → invalid.




5. Edge Cases
Empty string → valid.

Odd-length string → invalid.

Closing bracket first (e.g., ")") → invalid.

Key Takeaway
Stacks excel at order-sensitive problems (like nested brackets), while counters only track totals. Use a stack to ensure correct pairing and nesting.


after explaining the logic of the problem we'll move into the solution code :

![Alt text](/assets/img/photo.jpg)