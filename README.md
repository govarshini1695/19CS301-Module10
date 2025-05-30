# 19CS301-Module10
###EX: 10.a  STACK

### Aim: To Write a python program to get the integer values from the user and push only the odd number into the stack and later pop the last 2 elements.

### Algorithm:
STEP 1: Start.
STEP 2: Create a list and a variable n.
STEP 3: Get the value of n from user.
STEP 4: Using loop append only odd elements in the stack.
STEP 5 : Using another loop using built-in pop operation pop the last two elements.
STEP 6: Print the result.
STEP 7 : Stop.

### Program:
```
l=[]
n=int(input())
for i in range(n):
    value=int(input())
    if value%2!=0:
        l.append(value)
print(l)

for i in range(2):
    l.pop()
print(l)
```
### Output:
 ![image](https://github.com/user-attachments/assets/d2ce0434-7594-41af-ba20-3d7ecf9e0d93)

### Result: Thus, the given program is implemented and executed successfully .
 


### EX: 10.2 IMPLEMENTATION OF STACK

### Aim: To Write a python program to implement the stack using deque method for rotating the stack.

### Algorithm:

STEP 1: Start.
STEP 2: Import collections and import deque.
STEP 3: Create a list and get the input from user.
STEP 4: Create a variable n and get number of inputs from user.
STEP 5 : Using a loop get the inputs from user and append in deque.
STEP 6: Using rotate function rotate the stack.
STEP 7 : Print the result. 
STEP 8 : Stop.

### Program: 
```
import collections
def fun(r):
    de = collections.deque([])
    n=int(input())
    for i in range(n):
        de.append(float(input()))
    print("Stack before rotation",de)
    de.rotate(r)
    print("Stack after rotation",de)

```
### Output:
![image](https://github.com/user-attachments/assets/f42c4ec6-578c-418a-8f66-cf70abe7dc54)

### Result: Thus, the given program is implemented and executed successfully .
 


EX: 10.3 QUEUE

### Aim: To Write a python program to add only the even unique numbers using appendleft() from n given numbers. 

### Algorithm:
STEP 1:Initialize a set unique_evens to store unique even numbers.
STEP 2:Initialize a deque result to store the final sequence.
STEP 3:Iterate through the given list of numbers
STEP 4:Check if the number is even (num % 2 == 0).
STEP 5:Check if the number is not already in unique_evens.
STEP 6:If both conditions are met, add the number to unique_evens.
STEP 7:Use appendleft() to insert it at the front of result.
STEP 8:Return the final deque containing only unique even numbers in reverse order of their appearance.

### Program:
```
from collections import deque
class Queue:
    def __init__(self):
        self.queue = deque()
    def add_element(self,val):
        if val%2==0 and val not in self.queue:
            self.queue.appendleft(val)
            return True
        return False
TheQueue=Queue()
n=int(input())
for i in range(n):
    TheQueue.add_element(int(input()))
print(TheQueue.queue)

```

### Output:
![image](https://github.com/user-attachments/assets/de6e3e09-b10b-42d4-9faf-32fcf990f29a)
 
### Result: Thus, the given program is implemented and executed successfully .


### EX: 10.4 IMPLEMENTATION OF QUEUE

### Aim: To Develop a python program to Reverse values in Queue.

### Algorithm:

STEP 1:Start.
STEP 2:Initialize an empty stack to temporarily store the elements.
STEP 3:Dequeue all elements from the queue and push them onto the stack.
STEP 4:Pop elements from the stack one by one and enqueue them back into the queue.
STEP 5:Return the queue, now with reversed elements.
STEP 6:Print the result.
STEP 7:Stop.

### Program:
```
import queue
q1=queue.Queue()
for i in range(5):
    q1.put(int(input()))
    
def reverseQueue(q1src,q2dest):
    buffer=q1src.get()
    if (q1src.empty()==False):
        reverseQueue(q1src,q2dest)
    q2dest.put(buffer)
    return q2dest
    
q2dest=queue.Queue()
qReversed=reverseQueue(q1,q2dest)

while (qReversed.empty()==False):
    print(qReversed.queue[0])
    qReversed.get()
 
```
### Output:
![image](https://github.com/user-attachments/assets/f8e67e5a-a732-4987-a55f-4e7429e8bd98)

### Result: Thus, the given program is implemented and executed successfully .
 
SEB-STACK

AIM:
To write a python program to create a stack with a maximum size of 7 using Lifo Queue. 

ALGORITHM:
STEP 1:Start the program.
STEP 2:Create a stack with a maximum size of 7 using queue.LifoQueue.
STEP 3:Accept user input until the stack reaches its maximum capacity.
STEP 4:Check if the stack is full using the .full() method.
STEP 5:Display the values in reverse order using .get(), which follows Last-In-First-Out (LIFO) 
behavior.

PROGRAM:

```
from queue import LifoQueue
stack = LifoQueue(maxsize=7)
n=int(input())
for i in range(n):
    stack.put(input())
print(stack.full())
for i in range(n):
    print(stack.get())
```

OUTPUT:

![image](https://github.com/user-attachments/assets/6637fb74-8346-4981-9950-31c86cc548fb)

RESULT:
Thus the python program to create a stack with a maximum size of 7 using Lifo Queue is executed 
successfully.

