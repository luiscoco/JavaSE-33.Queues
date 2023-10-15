# JavaSE-Queues

In Java, a queue is a data structure that follows the First-In-First-Out (FIFO) principle, meaning that the first element added to the queue will be the first one to be removed.

## 1. Queue (LinkedList)

Java provides a Queue interface that extends the Collection interface.

Here's a simple example using the LinkedList class, which implements the Queue interface:

```java
import java.util.LinkedList;
import java.util.Queue;

public class QueueExample {
    public static void main(String[] args) {
        // Creating a Queue using LinkedList
        Queue<String> queue = new LinkedList<>();

        // Adding elements to the Queue
        queue.add("Element 1");
        queue.add("Element 2");
        queue.add("Element 3");

        System.out.println("Queue: " + queue);

        // Removing an element from the front of the Queue
        String removedElement = queue.poll();
        System.out.println("Removed Element: " + removedElement);
        System.out.println("Updated Queue: " + queue);

        // Peeking at the front element without removing it
        String frontElement = queue.peek();
        System.out.println("Front Element: " + frontElement);
        System.out.println("Queue after peek: " + queue);
    }
}
```

We create a Queue using LinkedList.

Elements are added to the queue using the add method.

We print the queue.

We use the poll method to remove the front element from the queue.

Print the removed element and the updated queue.

Use the peek method to look at the front element without removing it.

Print the front element and the queue after peeking.

Output:
```
Queue: [Element 1, Element 2, Element 3]
Removed Element: Element 1
Updated Queue: [Element 2, Element 3]
Front Element: Element 2
Queue after peek: [Element 2, Element 3]
```
This demonstrates the basic operations of adding, removing, and peeking at elements in a queue in Java.

## 2. ArrayDeque

Implementation: ArrayDeque is implemented as a resizable array. It allows dynamic resizing of the array to accommodate elements.

Performance: Offers O(1) time complexity for adding/removing elements from both ends (front and rear). This makes it very efficient for queue operations.

Usage: If you need a fast and efficient queue and the size of the queue is known or can be estimated, ArrayDeque is a good choice.

```java
import java.util.ArrayDeque;
import java.util.Queue;

public class ArrayDequeExample {
    public static void main(String[] args) {
        // Creating a Queue using ArrayDeque
        Queue<String> arrayDequeQueue = new ArrayDeque<>();

        arrayDequeQueue.add("Element 1");
        arrayDequeQueue.add("Element 2");
        arrayDequeQueue.add("Element 3");

        System.out.println("ArrayDeque Queue: " + arrayDequeQueue);
    }
}
```

## 3. LinkedList:
Implementation: LinkedList is implemented as a doubly-linked list. It provides a flexible structure where elements can be efficiently inserted or removed from both ends.

Performance: While it offers O(1) time complexity for adding/removing elements from the front, adding/removing from the rear has O(1) time complexity as well. 

However, accessing elements by index has O(n) time complexity.

Usage: If you need a more flexible data structure, and you'll be frequently adding/removing elements from both ends, LinkedList might be a good choice.

```java
import java.util.LinkedList;
import java.util.Queue;

public class LinkedListExample {
    public static void main(String[] args) {
        // Creating a Queue using LinkedList
        Queue<String> linkedListQueue = new LinkedList<>();

        linkedListQueue.add("Element 1");
        linkedListQueue.add("Element 2");
        linkedListQueue.add("Element 3");

        System.out.println("LinkedList Queue: " + linkedListQueue);
    }
}
```

In summary, choose ArrayDeque for a more memory-efficient and faster queue if you know the size or can estimate it. 

Choose LinkedList if you need flexibility in adding/removing elements from both ends, and the constant time complexity is acceptable for your use case.
