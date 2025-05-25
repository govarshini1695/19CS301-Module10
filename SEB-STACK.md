STACK

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
