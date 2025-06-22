---
title: " implementing queue using stack "
date: 2023-06-03 00:00:00 +0000
categories: [leetcode problems]
tags: [algorithmes]
---

# let's get started 

first we need to understand queues , stacks were already covered in previous problems 

so What's a queue ?

A queue is like waiting in line. The first one in is the first one out - that's FIFO. You add new items to the back (enqueue) and take items from the front (dequeue). Once something leaves the queue, it's gone

Why FIFO?

Order matters in scenarios like:

-Printer queues (first print job gets printed first)

-CPU scheduling (oldest tasks get processed first)

Key Behavior :

Once an element is processed, it's removed from the queue

Just like people leave a line after being served

The queue doesn't keep processed elements


solution code : 

![alt text](/assets/img/image.jpg)

explanation : 

basically using an input stack that we push into and output stack where we pop from simulates the behavior of the queue as for the complexity its an O(1) ammortized because when the output stack is empty we need to transfer elements from the input stack to it wich is an O(n) that makes the whole process an O(1) amortrized 
for more details ill add this first prototype i wrote with comments that follows my explanation : 


![alt text](/assets/img/image2.png)
