

## **📖 Java Collection Framework - Complete Guide (Basic to Advanced)**  

### **📌 Chapter 1: Introduction to Java Collection Framework**  
- What is a Collection?  
- Need for Collections over Arrays  
- Java Collection Framework Overview  
- Benefits of Using Collections  
- Collection Framework Hierarchy  

---

### **📌 Chapter 2: Iterable and Collection Interface**  
- Understanding `Iterable<T>`  
- Methods of the `Iterable` Interface  
- Understanding `Collection<T>` Interface  
- Important Methods of `Collection` Interface  

---

### **📌 Chapter 3: List Interface (Ordered Collection)**  
- Introduction to `List<T>` Interface  
- Implementations:  
  - `ArrayList` (Dynamic Array, Fast Read)  
  - `LinkedList` (Doubly Linked List, Fast Insert/Delete)  
  - `Vector` (Thread-Safe, Legacy)  
  - `Stack` (LIFO, Legacy)  
  - `CopyOnWriteArrayList` (Thread-Safe Variant of ArrayList)  
- **Operations on List** (Add, Remove, Search, Sort)  
- **Performance Comparison of List Implementations**  

---

### **📌 Chapter 4: Set Interface (Unique Elements Collection)**  
- Introduction to `Set<T>` Interface  
- Implementations:  
  - `HashSet` (Unordered, Unique, Uses Hashing)  
  - `LinkedHashSet` (Maintains Insertion Order)  
  - `TreeSet` (Sorted, Uses Red-Black Tree)  
  - `EnumSet` (Efficient Enum Collection)  
  - `ConcurrentSkipListSet` (Thread-Safe Sorted Set)  
  - `CopyOnWriteArraySet` (Thread-Safe Set)  
- **Set Operations (Union, Intersection, Difference, Subset)**  

---

### **📌 Chapter 5: Queue Interface (FIFO Data Structure)**  
- Introduction to `Queue<T>` Interface  
- Implementations:  
  - `LinkedList` (Can Be Used as Queue)  
  - `PriorityQueue` (Min-Heap Implementation)  
  - `Deque` (Double-Ended Queue)  
  - `ArrayDeque` (Resizable Array-Based Deque)  
  - `ConcurrentLinkedQueue` (Thread-Safe Queue)  
  - **BlockingQueues (Used in Multi-threading)**:  
    - `BlockingQueue` (Interface Overview)  
    - `ArrayBlockingQueue`  
    - `LinkedBlockingQueue`  
    - `PriorityBlockingQueue`  
    - `SynchronousQueue`  
    - `DelayQueue`  

---

### **📌 Chapter 6: Map Interface (Key-Value Pair Collection)**  
- Introduction to `Map<K, V>` Interface  
- Implementations:  
  - `HashMap` (Unordered Key-Value Mapping)  
  - `LinkedHashMap` (Maintains Insertion Order)  
  - `TreeMap` (Sorted Key-Value Mapping)  
  - `Hashtable` (Thread-Safe, Legacy)  
  - `ConcurrentHashMap` (Thread-Safe HashMap)  
- **Map Operations (Put, Get, Remove, Search, Iterate)**  

---

### **📌 Chapter 7: Comparators and Sorting in Collections**  
- `Comparable<T>` Interface (Natural Sorting)  
- `Comparator<T>` Interface (Custom Sorting)  
- Sorting Lists, Sets, and Maps with Comparators  

---

### **📌 Chapter 8: Collections Utility Class (Helper Methods)**  
- Sorting Collections (`Collections.sort()`)  
- Searching in Collections (`Collections.binarySearch()`)  
- Immutable Collections (`Collections.unmodifiableList()`)  
- Thread-Safe Collections (`Collections.synchronizedList()`)  

---

### **📌 Chapter 9: Thread-Safety in Java Collections**  
- Synchronization and Concurrent Collections  
- `CopyOnWriteArrayList`, `CopyOnWriteArraySet`  
- `ConcurrentHashMap`, `ConcurrentSkipListSet`  
- Performance Comparison of Synchronized and Concurrent Collections  

---

### **📌 Chapter 10: Best Practices and Performance Optimization**  
- When to Use Which Collection?  
- Performance Considerations for Different Data Structures  
- Avoiding `NullPointerException` in Collections  
- Optimizing Memory and CPU Usage in Collections  

---

Alright! Let’s go **step by step** and explain **Chapter 1: Introduction to Java Collection Framework** in a **very deep and easy way** so that you can **understand clearly** as a beginner. 🚀  

---

# **📌 Chapter 1: Introduction to Java Collection Framework**  

## **1️⃣ What is a Collection?**  
A **collection** in Java is a **group of objects** stored together. It helps in **storing, retrieving, manipulating, and processing** data efficiently.  

Think of a **collection** as a **container** (like a box) where you can store multiple objects.  

### **📍 Example:**
Imagine you have a list of student names. You can store them using **collections** instead of creating multiple variables.  

```java
List<String> students = new ArrayList<>();
students.add("John");
students.add("Emma");
students.add("David");
```
Here, `students` is a **collection** that stores multiple student names **together**.

### **💡 Key Features of Collections:**
✔ **Dynamic Size** - Unlike arrays, collections can grow and shrink in size dynamically.  
✔ **Efficient Operations** - Collections provide powerful methods for searching, sorting, and filtering data.  
✔ **Flexible Data Structures** - Supports different structures like **lists, sets, and queues**.  

---

## **2️⃣ Need for Collections over Arrays**  
Before collections, **arrays** were the only way to store multiple elements in Java. But arrays have some **limitations**.  

### **❌ Limitations of Arrays:**
1️⃣ **Fixed Size** - Once an array is created, its size **cannot** be changed.  
2️⃣ **No Built-in Methods** - Arrays do not provide methods for common tasks like searching or sorting.  
3️⃣ **Only Works with Indexes** - Arrays can only be accessed using **index numbers**, which is not always convenient.  
4️⃣ **Inefficient Insertion/Deletion** - Adding or removing elements in the middle of an array is difficult.  

### **✅ Why Collections are Better?**
✔ **Dynamic Size** - Collections **automatically resize** when adding/removing elements.  
✔ **Rich APIs** - Collections have built-in methods for sorting, searching, and filtering.  
✔ **More Flexibility** - Collections support different data structures like **lists, sets, and queues**.  
✔ **Easy to Use** - No need to manually manage indexes; you can directly use powerful methods.  

---

## **3️⃣ Java Collection Framework Overview**  
The **Java Collection Framework (JCF)** is a set of **predefined classes and interfaces** that help store and process data efficiently.  

It provides **ready-made implementations** for **Lists, Sets, Queues, and Maps**, so we don’t have to create them from scratch.  

### **🛠 Components of Java Collection Framework:**
1️⃣ **Interfaces** - Define the structure (e.g., `List`, `Set`, `Queue`, `Map`).  
2️⃣ **Classes** - Implement the interfaces (e.g., `ArrayList`, `HashSet`, `LinkedList`).  
3️⃣ **Methods** - Predefined operations (e.g., `add()`, `remove()`, `contains()`, `sort()`).  

---

## **4️⃣ Benefits of Using Collections**  

### **1️⃣ Dynamic Memory Allocation**
Unlike arrays, collections do not require a **fixed size** at the beginning. They **grow and shrink** dynamically as needed.  

### **2️⃣ Predefined Methods**
Collections provide **built-in methods** like `add()`, `remove()`, `contains()`, `size()`, making operations **easier**.  

### **3️⃣ Better Performance**
Collections are optimized for **fast searching, insertion, and deletion** operations compared to arrays.  

### **4️⃣ Easy Iteration**
Collections support **iterators** and **enhanced for-loops**, making traversal **simpler**.  

```java
for (String name : students) {
    System.out.println(name);
}
```
This is much easier compared to using **indexes in arrays**.

### **5️⃣ Supports Thread Safety**
Java provides **thread-safe** collections like `Vector` and `ConcurrentHashMap`, making them **safe for multi-threading**.

---

## **5️⃣ Collection Framework Hierarchy (Complete Structure)**  
The **Java Collection Framework** is structured as follows:

### **📌 Main Interfaces:**
1️⃣ **Iterable** - The root interface for all collections.  
2️⃣ **Collection** - Extends `Iterable` and is the base for `List`, `Set`, and `Queue`.  
3️⃣ **Map** - Stores data in **key-value pairs** (not part of `Collection`).  

### **📌 Collection Types:**
#### 🔹 **List (Ordered, Allows Duplicates)**
- `ArrayList`
- `LinkedList`
- `Vector`
- `Stack`
- `CopyOnWriteArrayList`

#### 🔹 **Set (Unique Elements, No Duplicates)**
- `HashSet`
- `LinkedHashSet`
- `TreeSet`
- `EnumSet`
- `CopyOnWriteArraySet`

#### 🔹 **Queue (FIFO Data Structure)**
- `PriorityQueue`
- `ArrayDeque`
- `BlockingQueue` (for multi-threading)

#### 🔹 **Map (Key-Value Pair Collection)**
- `HashMap`
- `LinkedHashMap`
- `TreeMap`
- `Hashtable`
- `ConcurrentHashMap`

---

## **📌 Summary of Chapter 1**
| Feature            | Arrays           | Collections |
|-------------------|----------------|-------------|
| **Size** | Fixed | Dynamic |
| **Built-in Methods** | No | Yes |
| **Efficiency** | Low (Slow Insert/Delete) | High (Optimized) |
| **Thread Safety** | No | Yes (Some classes) |
| **Data Structure Options** | Only One (Array) | List, Set, Queue, Map |

### **🌟 Key Takeaways:**
✔ **Collections are more powerful than arrays** because they provide **flexibility and efficiency**.  
✔ The **Java Collection Framework (JCF)** provides **ready-made classes and methods** for handling data efficiently.  
✔ Different **types of collections** (`List`, `Set`, `Queue`, `Map`) are available for different use cases.  

---


# **📌 Chapter 2: Iterable and Collection Interface**  

## **1️⃣ Understanding `Iterable<T>` Interface**  

### **📍 What is `Iterable<T>`?**  
- `Iterable<T>` is the **root interface** of the Java Collection Framework.  
- It **allows collections to be iterated (looped) using a `for-each` loop**.  
- All major collection classes like `ArrayList`, `LinkedList`, `HashSet`, etc., implement `Iterable<T>`.  

### **📍 Why is `Iterable<T>` Important?**  
1️⃣ It allows **for-each loop** to work on collections.  
2️⃣ It provides an `Iterator` to iterate through elements **one by one**.  

### **📍 Simple Example of `Iterable<T>`**
```java
import java.util.*;

public class IterableExample {
    public static void main(String[] args) {
        List<String> students = new ArrayList<>();
        students.add("Alice");
        students.add("Bob");
        students.add("Charlie");

        // Using for-each loop (Internally uses Iterable)
        for (String name : students) {
            System.out.println(name);
        }
    }
}
```
✅ **Here, `ArrayList` implements `Iterable<T>`**, so we can use a **for-each loop** to iterate through elements.  

---

## **2️⃣ Methods of the `Iterable<T>` Interface**  

The `Iterable<T>` interface provides **only one method** that must be implemented:  

### **🔹 `Iterator<T> iterator()`**
- Returns an **Iterator** to go through elements one by one.  
- The `Iterator` provides **three important methods**:  

| Method | Description |
|--------|-------------|
| `hasNext()` | Returns `true` if more elements are present. |
| `next()` | Returns the next element. |
| `remove()` | Removes the current element. |

### **📍 Example: Using `Iterator`**
```java
import java.util.*;

public class IteratorExample {
    public static void main(String[] args) {
        List<Integer> numbers = new ArrayList<>(Arrays.asList(10, 20, 30, 40));

        Iterator<Integer> it = numbers.iterator();  // Getting the iterator

        while (it.hasNext()) {  // Checking if more elements exist
            System.out.println(it.next());  // Printing the next element
        }
    }
}
```
✅ **Here, we manually iterate over `ArrayList` using an `Iterator`.**  

---

## **3️⃣ Understanding `Collection<T>` Interface**  

### **📍 What is `Collection<T>`?**  
- The `Collection<T>` interface **extends `Iterable<T>`**.  
- It provides **basic functionalities** for handling collections of objects.  
- **All major collection types (`List`, `Set`, `Queue`) implement `Collection<T>`.**  

### **📍 Key Features of `Collection<T>`**
✔ Allows adding and removing elements.  
✔ Supports operations like checking size, clearing the collection, and checking if it's empty.  
✔ Implements `Iterable<T>`, so it can be used in a **for-each loop**.  

### **📍 Collection Interface Hierarchy**
```
Iterable<T>
   │
   ├── Collection<T> 
         ├── List<T>  (Ordered, Duplicates Allowed)
         ├── Set<T>  (Unordered, Unique Elements)
         ├── Queue<T>  (FIFO)
```
✅ **So, every `List`, `Set`, and `Queue` class is part of `Collection<T>`.**  

### **📍 Example: Using `Collection<T>` Methods**
```java
import java.util.*;

public class CollectionExample {
    public static void main(String[] args) {
        Collection<String> names = new ArrayList<>();  // Collection interface reference
        names.add("John");
        names.add("Emma");
        names.add("David");

        System.out.println("Collection: " + names);
    }
}
```
✅ **Even though `Collection` is an interface, we can use `ArrayList` as an implementation.**  

---

## **4️⃣ Important Methods of `Collection<T>` Interface**  

The `Collection<T>` interface provides **various useful methods**. Let’s discuss the most important ones:  

| Method | Description |
|--------|-------------|
| `add(T element)` | Adds an element to the collection. |
| `remove(Object obj)` | Removes an element from the collection. |
| `size()` | Returns the number of elements in the collection. |
| `clear()` | Removes all elements from the collection. |
| `contains(Object obj)` | Checks if a specific element exists. |
| `isEmpty()` | Returns `true` if the collection is empty. |

### **📍 Example: Using Collection Methods**
```java
import java.util.*;

public class CollectionMethodsExample {
    public static void main(String[] args) {
        Collection<String> names = new ArrayList<>();
        names.add("Alice");
        names.add("Bob");
        names.add("Charlie");

        System.out.println("Size: " + names.size());  // 3
        System.out.println("Contains Bob? " + names.contains("Bob"));  // true
        names.remove("Bob");
        System.out.println("After removal: " + names);
        names.clear();
        System.out.println("Is collection empty? " + names.isEmpty());  // true
    }
}
```
✅ **Here, we added elements, checked their existence, removed an element, and cleared the collection.**  

---

## **📌 Summary of Chapter 2**
| Feature | `Iterable<T>` | `Collection<T>` |
|----------|-------------|--------------|
| **What is it?** | Root interface for iteration | Extends `Iterable`, supports basic collection operations |
| **Key Method(s)** | `iterator()` | `add()`, `remove()`, `size()`, `clear()`, `contains()` |
| **Usage** | Enables `for-each` loops | Used for storing and managing collections |
| **Implemented By** | `Collection`, `List`, `Set`, `Queue` | `ArrayList`, `HashSet`, `LinkedList`, etc. |

### **🌟 Key Takeaways:**
✔ **`Iterable<T>` is the root interface** that allows iteration through collections.  
✔ **`Collection<T>` extends `Iterable<T>` and adds basic collection functionalities.**  
✔ `Collection` provides important methods like `add()`, `remove()`, `size()`, `clear()`, and `contains()`.  
✔ **All major collection types (`List`, `Set`, `Queue`) implement `Collection<T>`.**  

---



# **📌 Chapter 3: List Interface (Ordered Collection)**  

## **1️⃣ Understanding `List<T>` Interface**  

### **📍 What is `List<T>`?**  
- `List<T>` is an **ordered collection** in Java that allows **duplicate elements**.  
- It extends the `Collection<T>` interface.  
- **Order matters** in `List`, meaning elements are stored in the same sequence in which they are inserted.  
- Unlike `Set<T>`, it **allows duplicate values**.  

### **📍 Characteristics of `List<T>`**
✅ **Maintains Insertion Order** – Elements are stored in the order they were added.  
✅ **Allows Duplicates** – You can have multiple occurrences of the same element.  
✅ **Indexed Access** – Elements can be accessed using **index positions (0, 1, 2, ...)**.  
✅ **Can Contain `null` Values** – Unlike some `Set` implementations, `List` can store `null`.  

### **📍 List Interface Hierarchy**
```
Iterable<T>
   │
   ├── Collection<T>
         │
         ├── List<T>  (Ordered, Duplicates Allowed)
                ├── ArrayList<T>  (Fast Read, Dynamic Array)
                ├── LinkedList<T>  (Fast Insert/Delete, Doubly Linked List)
                ├── Vector<T>  (Thread-Safe, Legacy)
                ├── Stack<T>  (LIFO, Legacy)
                ├── CopyOnWriteArrayList<T>  (Thread-Safe Variant of ArrayList)
```
✅ **So, every `ArrayList`, `LinkedList`, `Vector`, and `Stack` is a part of `List<T>`.**  

---

## **2️⃣ Methods of `List<T>` Interface**  

The `List<T>` interface provides various useful methods:  

| Method | Description |
|--------|-------------|
| `add(T element)` | Adds an element to the list. |
| `add(int index, T element)` | Inserts an element at a specific index. |
| `remove(int index)` | Removes the element at a given index. |
| `remove(Object obj)` | Removes the first occurrence of a specified object. |
| `get(int index)` | Retrieves the element at a specific index. |
| `set(int index, T element)` | Replaces the element at the given index. |
| `indexOf(T element)` | Returns the first index of an element (or `-1` if not found). |
| `lastIndexOf(T element)` | Returns the last index of an element. |
| `subList(int fromIndex, int toIndex)` | Extracts a portion of the list. |
| `sort(Comparator<T> c)` | Sorts the list using a comparator. |

---

## **3️⃣ Example: Basic Operations with `List<T>`**  

### **📍 Example: Using `ArrayList` as `List`**
```java
import java.util.*;

public class ListExample {
    public static void main(String[] args) {
        List<String> names = new ArrayList<>();  // Using List<T> reference
        names.add("Alice");
        names.add("Bob");
        names.add("Charlie");
        names.add("Alice");  // Duplicates allowed

        System.out.println("List: " + names);  // [Alice, Bob, Charlie, Alice]

        System.out.println("Element at index 1: " + names.get(1));  // Bob

        names.remove(2);  // Removing "Charlie"
        System.out.println("After removal: " + names);  // [Alice, Bob, Alice]

        names.set(1, "David");  // Replacing "Bob" with "David"
        System.out.println("After set: " + names);  // [Alice, David, Alice]
    }
}
```

---

## **4️⃣ Implementations of `List<T>` Interface**  

The `List<T>` interface has multiple implementations. Let’s discuss each one in detail.  

### **📌 1. `ArrayList<T>` (Dynamic Array, Fast Read)**  
- Uses **dynamic array** to store elements.  
- **Fast retrieval (O(1))**, but **slower insertion & deletion (O(n))**.  
- **Best when searching elements frequently**.  
- **Not thread-safe** (use `CopyOnWriteArrayList` for thread safety).  

### **📌 2. `LinkedList<T>` (Doubly Linked List, Fast Insert/Delete)**  
- Uses **doubly linked list** to store elements.  
- **Fast insertion & deletion (O(1))**, but **slower retrieval (O(n))**.  
- **Best when adding/removing elements frequently**.  
- **Not thread-safe** (explicit synchronization needed).  

### **📌 3. `Vector<T>` (Thread-Safe, Legacy)**  
- Similar to `ArrayList`, but **synchronized (thread-safe)**.  
- **Slower than `ArrayList` due to synchronization overhead**.  
- **Rarely used** today (use `CopyOnWriteArrayList` instead).  

### **📌 4. `Stack<T>` (LIFO, Legacy)**  
- **Follows Last-In-First-Out (LIFO) order**.  
- Used for **stack operations like undo, recursion, and function calls**.  
- Internally extends `Vector<T>`, making it **thread-safe**.  

### **📌 5. `CopyOnWriteArrayList<T>` (Thread-Safe Variant of `ArrayList`)**  
- **Best for concurrent applications** where **read operations are more frequent**.  
- Each modification creates a **new copy of the list**, avoiding concurrent modification issues.  
- **Higher memory consumption** due to copying.  

---

## **📌 Summary of `List<T>` Implementations**  

| Implementation | Internal Structure | Performance | Thread Safety | Best Use Case |
|---------------|-------------------|-------------|--------------|--------------|
| **ArrayList** | Dynamic Array | Fast Read (O(1)), Slow Insert/Delete (O(n)) | ❌ No | Frequent Read Operations |
| **LinkedList** | Doubly Linked List | Slow Read (O(n)), Fast Insert/Delete (O(1)) | ❌ No | Frequent Insert/Delete |
| **Vector** | Dynamic Array | Similar to `ArrayList`, but slower due to synchronization | ✅ Yes | Legacy Code, Multi-threading |
| **Stack** | Dynamic Array (LIFO) | LIFO operations, similar to `Vector` | ✅ Yes | Stack Operations (Undo, Function Calls) |
| **CopyOnWriteArrayList** | Dynamic Array (Copy on Write) | Fast Read, Slow Write | ✅ Yes | Concurrent Read Operations |

---

## **📌 Key Takeaways**
✔ **`List<T>` is an ordered collection that allows duplicates and indexed access.**  
✔ It has multiple implementations:  
  - **`ArrayList`** (Fast read, slow insert/delete)  
  - **`LinkedList`** (Slow read, fast insert/delete)  
  - **`Vector`** (Thread-safe, legacy)  
  - **`Stack`** (LIFO structure)  
  - **`CopyOnWriteArrayList`** (Thread-safe variant of `ArrayList`)  
✔ Choose the right `List<T>` implementation based on **performance needs**.  

---


# **📌 ArrayList<T> (Dynamic Array, Fast Read)**  

## **1️⃣ What is `ArrayList<T>`?**  
- `ArrayList<T>` is a **dynamic array implementation** of the `List<T>` interface.  
- It can **grow and shrink dynamically** based on the number of elements.  
- **Fast read operations (O(1))**, but **slower insert/delete (O(n))** compared to `LinkedList`.  
- It **allows duplicate elements** and **maintains insertion order**.  

---

## **2️⃣ How `ArrayList<T>` Works Internally?**  
📌 **Internal Structure**  
- `ArrayList` internally uses an **array** to store elements.  
- When the **capacity is full**, it **creates a new array** with **1.5x larger size** and **copies old elements into it**.  
- This is why `ArrayList` is **fast for reading**, but **slow for insertion/deletion at the beginning or middle**.  

🛠 **Example:**  
If an `ArrayList` has **capacity 10**, and we try to add the 11th element:  
- Java **creates a new array of size 15 (1.5x of 10)**.  
- It **copies old 10 elements** into the new array.  
- It **adds the 11th element** in the newly allocated space.  

✅ **This process is called "dynamic resizing".**  

---

## **3️⃣ How to Create an `ArrayList<T>`?**  

### **📍 Creating an `ArrayList` in Java**
```java
import java.util.*;

public class ArrayListExample {
    public static void main(String[] args) {
        ArrayList<String> names = new ArrayList<>(); // Creating an empty ArrayList
        names.add("Alice");
        names.add("Bob");
        names.add("Charlie");

        System.out.println("ArrayList: " + names);  // [Alice, Bob, Charlie]
    }
}
```
✅ **Here, we created an `ArrayList<String>` and added elements.**  

---

## **4️⃣ ArrayList Methods (With Examples)**  

### **📌 1. `add(E element)` → Add element to the list**  
Adds an element at the **end of the list**.  
```java
ArrayList<String> list = new ArrayList<>();
list.add("Java");
list.add("Python");
System.out.println(list);  // Output: [Java, Python]
```

---

### **📌 2. `add(int index, E element)` → Insert at a specific index**  
Inserts an element at the given **index** (shifts existing elements).  
```java
ArrayList<String> list = new ArrayList<>();
list.add("Java");
list.add("Python");
list.add(1, "C++");  // Insert "C++" at index 1
System.out.println(list);  // Output: [Java, C++, Python]
```
⏳ **Time Complexity:** `O(n)`, because elements need to shift.

---

### **📌 3. `get(int index)` → Retrieve element at index**  
Gets the **element present at the given index**.  
```java
ArrayList<String> list = new ArrayList<>();
list.add("Java");
list.add("Python");
System.out.println(list.get(1));  // Output: Python
```
✅ **Fast (O(1)) since `ArrayList` provides direct access using an index.**

---

### **📌 4. `set(int index, E element)` → Update element at index**  
Replaces the element at the given **index** with a new value.  
```java
ArrayList<String> list = new ArrayList<>();
list.add("Java");
list.add("Python");
list.set(1, "C++");  // Replace Python with C++
System.out.println(list);  // Output: [Java, C++]
```
✅ **Efficient operation (O(1)).**  

---

### **📌 5. `remove(int index)` → Remove element by index**  
Removes the **element at the specified index**, shifting elements left.  
```java
ArrayList<String> list = new ArrayList<>();
list.add("Java");
list.add("Python");
list.add("C++");
list.remove(1);  // Remove "Python" (index 1)
System.out.println(list);  // Output: [Java, C++]
```
⏳ **Time Complexity:** `O(n)`, because elements shift left.

---

### **📌 6. `remove(Object obj)` → Remove element by value**  
Removes the **first occurrence** of the given value.  
```java
ArrayList<String> list = new ArrayList<>();
list.add("Java");
list.add("Python");
list.add("C++");
list.remove("Python");  // Remove "Python"
System.out.println(list);  // Output: [Java, C++]
```
✅ **Returns `true` if element was found and removed.**  

---

### **📌 7. `size()` → Get the number of elements**  
Returns the **total number of elements** in the list.  
```java
ArrayList<String> list = new ArrayList<>();
list.add("Java");
list.add("Python");
System.out.println(list.size());  // Output: 2
```

---

### **📌 8. `contains(E element)` → Check if element exists**  
Checks if the **list contains a specific element**.  
```java
ArrayList<String> list = new ArrayList<>();
list.add("Java");
list.add("Python");
System.out.println(list.contains("Python"));  // Output: true
System.out.println(list.contains("C++"));  // Output: false
```

---

### **📌 9. `indexOf(E element)` → Get index of first occurrence**  
Returns the **index of the first occurrence** of an element (`-1` if not found).  
```java
ArrayList<String> list = new ArrayList<>();
list.add("Java");
list.add("Python");
list.add("Java");
System.out.println(list.indexOf("Java"));  // Output: 0
System.out.println(list.indexOf("C++"));  // Output: -1 (not found)
```

---

### **📌 10. `lastIndexOf(E element)` → Get index of last occurrence**  
```java
ArrayList<String> list = new ArrayList<>();
list.add("Java");
list.add("Python");
list.add("Java");
System.out.println(list.lastIndexOf("Java"));  // Output: 2
```

---

### **📌 11. `subList(int fromIndex, int toIndex)` → Get portion of list**  
Extracts a **portion of the list** (from `fromIndex` to `toIndex-1`).  
```java
ArrayList<String> list = new ArrayList<>();
list.add("Java");
list.add("Python");
list.add("C++");
list.add("JavaScript");
System.out.println(list.subList(1, 3));  // Output: [Python, C++]
```

---

### **📌 12. `clear()` → Remove all elements**  
```java
ArrayList<String> list = new ArrayList<>();
list.add("Java");
list.add("Python");
list.clear();
System.out.println(list);  // Output: []
```

---

## **📌 When to Use `ArrayList<T>`?**
✔ **Best for fast random access (O(1)).**  
✔ **Use when searching elements frequently.**  
✔ **Avoid if you need frequent insertions/deletions in the middle.**  

---

## **📌 Summary**  

| Method | Description |
|--------|-------------|
| `add(E e)` | Adds an element to the end |
| `add(int index, E e)` | Inserts element at a specific index |
| `get(int index)` | Retrieves element at an index |
| `set(int index, E e)` | Replaces element at an index |
| `remove(int index)` | Removes element at index |
| `remove(Object obj)` | Removes first occurrence of element |
| `contains(E e)` | Checks if element exists |
| `size()` | Returns the number of elements |
| `clear()` | Removes all elements |
| `subList(int from, int to)` | Gets a portion of the list |

---

# **📌 Deep Dive into `LinkedList<T>` (Doubly Linked List, Fast Insert/Delete)**  

🚀 **In this chapter, we will explore `LinkedList<T>` in depth**. We will cover **how it works internally, when to use it, and all its methods with easy explanations and examples.**  

---

## **1️⃣ What is `LinkedList<T>`?**  
- `LinkedList<T>` is a **doubly linked list** implementation of the `List<T>` interface.  
- Unlike `ArrayList`, it does **not use an array internally**. Instead, it uses **nodes (objects) that are linked together**.  
- Each node contains **3 parts**:
  1. **Data (Element)**  
  2. **Reference to the next node**  
  3. **Reference to the previous node**  

🔗 **Structure of a LinkedList node:**  
```
[Prev | Data | Next]  <-->  [Prev | Data | Next]  <-->  [Prev | Data | Next]
```

✅ **Key Features of `LinkedList<T>`:**  
✔ **Fast insertions and deletions (`O(1)`)** at the beginning and middle.  
✔ **Slower searching (`O(n)`)** because elements are not indexed.  
✔ **Can be used as a `Queue` or `Stack` (since it has `addFirst()` and `removeFirst()`).**  

---

## **2️⃣ How `LinkedList<T>` Works Internally?**  
📌 `LinkedList<T>` maintains a reference to:  
- **First Node (`head`)** → Points to the first element.  
- **Last Node (`tail`)** → Points to the last element.  

### **Insertion Process:**  
- If inserting at the **beginning** (`addFirst()`), it updates the `head` to the new node.  
- If inserting at the **end** (`addLast()`), it updates the `tail` to the new node.  

### **Deletion Process:**  
- If deleting at the **beginning** (`removeFirst()`), the `head` moves to the next node.  
- If deleting at the **end** (`removeLast()`), the `tail` moves to the previous node.  

✅ **This makes insertion and deletion fast (`O(1)`).**  

---

## **3️⃣ How to Create a `LinkedList<T>`?**  
### **📍 Creating a `LinkedList` in Java**
```java
import java.util.LinkedList;

public class LinkedListExample {
    public static void main(String[] args) {
        LinkedList<String> names = new LinkedList<>(); // Creating a LinkedList
        names.add("Alice");
        names.add("Bob");
        names.add("Charlie");

        System.out.println("LinkedList: " + names);  // Output: [Alice, Bob, Charlie]
    }
}
```

✅ **Here, we created a `LinkedList<String>` and added elements.**  

---

## **4️⃣ `LinkedList<T>` Methods (With Examples)**  

### **📌 1. `add(E element)` → Add element at the end**  
Adds an element to the **end of the list**.  
```java
LinkedList<String> list = new LinkedList<>();
list.add("Java");
list.add("Python");
System.out.println(list);  // Output: [Java, Python]
```

---

### **📌 2. `add(int index, E element)` → Insert at a specific index**  
Inserts an element at the given **index** (shifts existing elements).  
```java
LinkedList<String> list = new LinkedList<>();
list.add("Java");
list.add("Python");
list.add(1, "C++");  // Insert "C++" at index 1
System.out.println(list);  // Output: [Java, C++, Python]
```
✅ **Faster than `ArrayList` for insertions in the middle (`O(1)`).**  

---

### **📌 3. `addFirst(E element)` → Insert at the beginning**  
Inserts an element **at the start of the list**.  
```java
LinkedList<String> list = new LinkedList<>();
list.add("Python");
list.addFirst("Java");  // Add "Java" at the beginning
System.out.println(list);  // Output: [Java, Python]
```

---

### **📌 4. `addLast(E element)` → Insert at the end**  
Same as `add()`, but explicitly adds at the end.  
```java
LinkedList<String> list = new LinkedList<>();
list.add("Python");
list.addLast("JavaScript");
System.out.println(list);  // Output: [Python, JavaScript]
```

---

### **📌 5. `get(int index)` → Retrieve element at index**  
Gets the **element present at the given index**.  
```java
LinkedList<String> list = new LinkedList<>();
list.add("Java");
list.add("Python");
System.out.println(list.get(1));  // Output: Python
```
❌ **Slower (`O(n)`) than `ArrayList` because it has to traverse the list.**  

---

### **📌 6. `getFirst()` → Get first element**  
```java
LinkedList<String> list = new LinkedList<>();
list.add("Java");
list.add("Python");
System.out.println(list.getFirst());  // Output: Java
```

---

### **📌 7. `getLast()` → Get last element**  
```java
LinkedList<String> list = new LinkedList<>();
list.add("Java");
list.add("Python");
System.out.println(list.getLast());  // Output: Python
```

---

### **📌 8. `remove(int index)` → Remove element by index**  
Removes the **element at the specified index**.  
```java
LinkedList<String> list = new LinkedList<>();
list.add("Java");
list.add("Python");
list.add("C++");
list.remove(1);  // Remove "Python" (index 1)
System.out.println(list);  // Output: [Java, C++]
```

---

### **📌 9. `remove(Object obj)` → Remove element by value**  
```java
LinkedList<String> list = new LinkedList<>();
list.add("Java");
list.add("Python");
list.remove("Python");  // Remove "Python"
System.out.println(list);  // Output: [Java]
```

---

### **📌 10. `removeFirst()` → Remove first element**  
```java
LinkedList<String> list = new LinkedList<>();
list.add("Java");
list.add("Python");
list.removeFirst();
System.out.println(list);  // Output: [Python]
```

---

### **📌 11. `removeLast()` → Remove last element**  
```java
LinkedList<String> list = new LinkedList<>();
list.add("Java");
list.add("Python");
list.removeLast();
System.out.println(list);  // Output: [Java]
```

---

### **📌 12. `size()` → Get the number of elements**  
```java
LinkedList<String> list = new LinkedList<>();
list.add("Java");
list.add("Python");
System.out.println(list.size());  // Output: 2
```

---

### **📌 13. `clear()` → Remove all elements**  
```java
LinkedList<String> list = new LinkedList<>();
list.add("Java");
list.add("Python");
list.clear();
System.out.println(list);  // Output: []
```

---

## **📌 When to Use `LinkedList<T>`?**
✔ **Best for fast insertions and deletions (`O(1)`).**  
✔ **Use when frequently adding/removing elements from the start or middle.**  
❌ **Avoid if you need fast random access (`O(n)`).**  

---

## **📌 Summary**  

| Method | Description |
|--------|-------------|
| `add(E e)` | Adds an element at the end |
| `addFirst(E e)` | Adds an element at the beginning |
| `get(int index)` | Retrieves element at an index |
| `remove(int index)` | Removes element at index |
| `removeFirst()` | Removes the first element |
| `removeLast()` | Removes the last element |
| `clear()` | Removes all elements |

---

# **📌 Deep Dive: How `LinkedList<T>` Works Internally in Java**  

🚀 In this section, we will **break down the internal working of `LinkedList<T>`** step by step.  
I will explain **how elements are stored, inserted, deleted, and accessed internally** using a **doubly linked list structure**.  

---

## **1️⃣ What is a Linked List?**  

A **Linked List** is a **linear data structure** that consists of a **sequence of nodes** where:  

1. **Each node stores two things:**
   - **Data** (the actual element)
   - **References (pointers) to the next and previous nodes**  

2. Unlike an **array**, which stores elements **contiguously in memory**, a **linked list stores elements in separate memory locations**, connected using pointers.  

### **📍 Structure of a `LinkedList<T>` Node:**  
Each node contains **three parts**:  
```
[Prev | Data | Next]
```
- **Prev** → Points to the **previous** node  
- **Data** → Stores the **actual value**  
- **Next** → Points to the **next** node  

### **📌 Example of a `LinkedList` with three elements:**  
```
Head -> [null | A | ⬇]  <-->  [⬆ | B | ⬇]  <-->  [⬆ | C | null] <- Tail
```
- **Head** points to the **first node (A)**  
- **Tail** points to the **last node (C)**  
- Each node is **connected both ways** (Doubly Linked List)  

---

## **2️⃣ How Java's `LinkedList<T>` Works Internally?**  

📌 **Java’s `LinkedList<T>` is implemented as a Doubly Linked List (`DLL`).**  
- The `LinkedList` class has **two important instance variables**:
  - `Node first` → **Points to the first node** (head)
  - `Node last` → **Points to the last node** (tail)  

📌 **Internal Node Class (`LinkedList.Node<T>`)**
```java
private static class Node<T> {
    T item;       // The actual data stored
    Node<T> next; // Pointer to the next node
    Node<T> prev; // Pointer to the previous node

    Node(Node<T> prev, T item, Node<T> next) {
        this.item = item;
        this.next = next;
        this.prev = prev;
    }
}
```
✅ **Each node stores:**  
- **Data (`item`)**
- **Next node reference (`next`)**
- **Previous node reference (`prev`)**  

---

## **3️⃣ How `add(E element)` Works Internally?**  

📌 **Adding elements to a `LinkedList` (appending to the end)**  
```java
LinkedList<String> list = new LinkedList<>();
list.add("A"); 
list.add("B");
list.add("C");
```

### **Step-by-Step Execution:**  
1. **First Element "A" is added** → A new node is created  
   ```
   [null | A | null] 
   ```
   - **Head and Tail both point to A**  

2. **Second Element "B" is added**  
   ```
   [null | A | ⬇]  <-->  [⬆ | B | null]  
   ```
   - **A’s `next` pointer points to B**  
   - **B’s `prev` pointer points to A**  
   - **Tail now points to B**  

3. **Third Element "C" is added**  
   ```
   [null | A | ⬇]  <-->  [⬆ | B | ⬇]  <-->  [⬆ | C | null]  
   ```
   - **B’s `next` pointer points to C**  
   - **C’s `prev` pointer points to B**  
   - **Tail now points to C**  

✅ **Insertion is O(1) because we only update pointers.**  

---

## **4️⃣ How `remove(E element)` Works Internally?**  

📌 **Removing an element from `LinkedList`**  
```java
list.remove("B");  // Remove "B"
```

### **Step-by-Step Execution:**  
Before removing:  
```
[null | A | ⬇]  <-->  [⬆ | B | ⬇]  <-->  [⬆ | C | null]
```
1. **Find "B"** → Traverse nodes until we reach "B"  
2. **Update Pointers**  
   - **A’s `next` now points to C**
   - **C’s `prev` now points to A**  
3. **Remove "B"**  

After removing "B":  
```
[null | A | ⬇]  <-->  [⬆ | C | null]
```

✅ **Removal is O(1) if we already have a reference, otherwise O(n) if we search first.**  

---

## **5️⃣ How `get(int index)` Works Internally?**  

📌 **Retrieving an element by index (`O(n)`)**  
```java
String value = list.get(2);  // Fetch element at index 2
```
1. **If `index < size/2`**, start from **head** and move forward  
2. **If `index > size/2`**, start from **tail** and move backward  

Example for `list.get(2)`:  
```
[null | A | ⬇]  <-->  [⬆ | B | ⬇]  <-->  [⬆ | C | null]
```
1. **Start from `head` and move `next` twice** → Reached C  
2. **Return C**  

✅ **Slower than `ArrayList` because there is no direct index access (O(n) complexity).**  

---

## **6️⃣ How `addFirst()` and `addLast()` Work?**  

📌 **`addFirst(E e)` → Adds element at the start**  
```java
list.addFirst("X");
```
Before:  
```
[null | A | ⬇]  <-->  [⬆ | B | ⬇]  <-->  [⬆ | C | null]
```
After adding `"X"` at the start:  
```
[null | X | ⬇]  <-->  [⬆ | A | ⬇]  <-->  [⬆ | B | ⬇]  <-->  [⬆ | C | null]
```
✅ **O(1) complexity since only head pointer changes.**  

📌 **`addLast(E e)` → Adds element at the end**  
```java
list.addLast("Y");
```
```
[null | X | ⬇]  <-->  [⬆ | A | ⬇]  <-->  [⬆ | B | ⬇]  <-->  [⬆ | C | ⬇]  <-->  [⬆ | Y | null]
```
✅ **O(1) complexity since only tail pointer changes.**  

---

## **7️⃣ Time Complexity Comparison**  

| Operation | LinkedList | ArrayList |
|-----------|-----------|-----------|
| Insert at End | O(1) | O(1) |
| Insert at Beginning | O(1) | O(n) |
| Insert in Middle | O(1) (if reference is known) | O(n) |
| Delete at Beginning | O(1) | O(n) |
| Delete at End | O(1) | O(1) |
| Delete in Middle | O(1) (if reference is known) | O(n) |
| Access (get) | O(n) | O(1) |

🔹 **LinkedList is better for frequent insertions and deletions.**  
🔹 **ArrayList is better for fast access (`get(index)`).**  

---

## **📌 Conclusion**
✅ **LinkedList<T> works internally as a doubly linked list.**  
✅ **Each node stores data, a pointer to the next node, and a pointer to the previous node.**  
✅ **Insertions and deletions are O(1) if the reference is known.**  
✅ **Retrieving elements by index is O(n) (slower than `ArrayList`).**  

---


# **📌 Deep Dive into `Vector<T>` in Java**  


## **1️⃣ What is a `Vector<T>`?**  

🔹 `Vector<T>` is a **dynamic array** in Java, just like `ArrayList<T>`, but with **one key difference**:  
**Vector is thread-safe** (i.e., multiple threads can access it safely).  

🔹 `Vector<T>` is a part of **Java's legacy collection framework**, but it is still used when we need **a synchronized (thread-safe) list**.  

🔹 **Package:**  
```java
import java.util.Vector;
```

---

## **2️⃣ Why Use `Vector<T>`?**  

💡 **Why do we need Vector when we have ArrayList?**  

✅ **Thread Safety**: `Vector<T>` is synchronized, so it can be used safely in multi-threaded environments.  

✅ **Dynamic Resizing**: Unlike an array, `Vector` grows dynamically when more elements are added.  

✅ **Fast Random Access**: Since it is an **array-based** structure, `Vector` allows fast access via an index.  

🚫 **But...**  
- **`Vector<T>` is slower than `ArrayList<T>`** because **each method in Vector is synchronized**, making it thread-safe but slower.  
- **If you don’t need thread safety, use `ArrayList<T>` instead.**  

---

## **3️⃣ Internal Working of `Vector<T>`**  

📌 **How `Vector<T>` stores elements internally?**  
- `Vector<T>` is implemented **internally as a resizable array**.  
- It has an **initial capacity** (default = 10), and when it is full, **it grows by doubling its size**.  

### **Internal Structure of `Vector<T>` (Before Resizing)**  
```
[ A ] [ B ] [ C ] [ D ] [ E ] [ - ] [ - ] [ - ] [ - ] [ - ]
(size = 5, capacity = 10)
```

### **After Adding More Elements (Resizing Happens)**  
```
[ A ] [ B ] [ C ] [ D ] [ E ] [ F ] [ G ] [ H ] [ I ] [ J ] 
(size = 10, capacity = 10)
```
✅ **If one more element is added, Vector resizes (doubles capacity from 10 → 20):**  
```
[ A ] [ B ] [ C ] [ D ] [ E ] [ F ] [ G ] [ H ] [ I ] [ J ] [ K ] [ - ] [ - ] [ - ] [ - ] [ - ] ...
(size = 11, capacity = 20)
```
📌 **Key Point:** Vector **doubles its capacity when it exceeds the limit**, while `ArrayList` grows by **50% of its size**.  

---

## **4️⃣ How to Create a `Vector<T>`?**  

### **📍 Default Constructor (Capacity = 10)**
```java
Vector<Integer> vector = new Vector<>();
```
📌 This creates a `Vector` with **default capacity = 10**.

---

### **📍 Specifying Initial Capacity**
```java
Vector<Integer> vector = new Vector<>(20);
```
📌 This creates a `Vector` with **initial capacity = 20**.

---

### **📍 Specifying Capacity Increment**
```java
Vector<Integer> vector = new Vector<>(10, 5);
```
📌 **Initial capacity = 10**  
📌 **Increases by 5 when full** (instead of doubling).  

---

## **5️⃣ Important Methods in `Vector<T>` (with Examples)**  

### **📍 1. `add(E e)` - Add an element at the end**
```java
Vector<String> vector = new Vector<>();
vector.add("A");
vector.add("B");
vector.add("C");
System.out.println(vector);  // Output: [A, B, C]
```

---

### **📍 2. `add(int index, E element)` - Insert at a specific position**
```java
vector.add(1, "X");  
System.out.println(vector);  // Output: [A, X, B, C]
```

---

### **📍 3. `get(int index)` - Retrieve element at index**
```java
String element = vector.get(2); 
System.out.println(element);  // Output: B
```

---

### **📍 4. `remove(int index)` - Remove element at index**
```java
vector.remove(1);  
System.out.println(vector);  // Output: [A, B, C]
```

---

### **📍 5. `remove(Object obj)` - Remove specific object**
```java
vector.remove("B");  
System.out.println(vector);  // Output: [A, C]
```

---

### **📍 6. `set(int index, E element)` - Replace an element**
```java
vector.set(1, "Z");  
System.out.println(vector);  // Output: [A, Z, C]
```

---

### **📍 7. `size()` - Get the number of elements**
```java
System.out.println(vector.size());  // Output: 3
```

---

### **📍 8. `capacity()` - Get current capacity**
```java
System.out.println(vector.capacity());  // Output: 10 (default)
```

---

### **📍 9. `isEmpty()` - Check if Vector is empty**
```java
System.out.println(vector.isEmpty());  // Output: false
```

---

### **📍 10. `contains(E e)` - Check if element exists**
```java
System.out.println(vector.contains("Z"));  // Output: true
```

---

### **📍 11. `clear()` - Remove all elements**
```java
vector.clear();
System.out.println(vector);  // Output: []
```

---

### **📍 12. `forEach()` - Iterate using forEach loop**
```java
vector.add("A");
vector.add("B");
vector.add("C");

vector.forEach(e -> System.out.println(e));  
// Output:
// A
// B
// C
```

---

## **6️⃣ Performance Comparison (`Vector<T>` vs `ArrayList<T>`)**  

| Operation | `Vector<T>` | `ArrayList<T>` |
|-----------|------------|---------------|
| Thread Safety | ✅ Yes (Synchronized) | ❌ No |
| Performance | 🚫 Slower | ✅ Faster |
| Resizing Policy | Doubles capacity | Increases by 50% |
| Random Access (`get(int)`) | ✅ O(1) | ✅ O(1) |
| Insert/Delete in Middle | 🚫 O(n) | 🚫 O(n) |
| Insert/Delete at End | ✅ O(1) | ✅ O(1) |

🚀 **Use `Vector<T>` only when thread safety is required.**  
🚀 **For better performance in single-threaded applications, use `ArrayList<T>`.**  

---

## **📌 Conclusion**
✅ `Vector<T>` is a **resizable array** that is **synchronized (thread-safe)**.  
✅ It has **slower performance** than `ArrayList<T>` due to **synchronization overhead**.  
✅ **Use `Vector<T>` when multiple threads modify the list simultaneously**.  
✅ **Prefer `ArrayList<T>` for better performance in a single-threaded environment**.  

---

# **📌 Deep Dive into `Stack<T>` in Java**  


## **1️⃣ What is a `Stack<T>`?**  

🔹 `Stack<T>` is a **Last In, First Out (LIFO)** data structure in Java.  
🔹 It is a **special type of `Vector<T>`** that **allows only specific operations**.  
🔹 The **last element added is the first to be removed** (just like a stack of plates 🍽️).  
🔹 **Stack is synchronized**, meaning it is **thread-safe**, but **slower than non-synchronized alternatives**.  

🔹 **Package:**  
```java
import java.util.Stack;
```

📌 **Key Concept: LIFO (Last In, First Out)**  
```
Push -> [ A ] [ B ] [ C ] (C is the last added)
Pop -> [ A ] [ B ] (C is removed first)
```

---

## **2️⃣ Why Use `Stack<T>`?**  

💡 **When should you use a Stack?**  

✅ **When you need LIFO order** (Last In, First Out).  
✅ **Undo/Redo operations** (e.g., in text editors).  
✅ **Browser back/forward history**.  
✅ **Expression evaluation** (e.g., parsing arithmetic expressions).  
✅ **Recursion tracking** (call stack in programming).  

🚫 **But...**  
- **Stack<T> is slower than alternatives like `Deque<T>`** because it is synchronized.  
- **For better performance, use `ArrayDeque<T>` instead of `Stack<T>`**.  

---

## **3️⃣ Internal Working of `Stack<T>`**  

📌 **How `Stack<T>` stores elements internally?**  
- `Stack<T>` extends `Vector<T>` → **It is a dynamic array** that resizes itself when full.  
- It provides **extra methods** like `push()`, `pop()`, `peek()`, etc., for stack operations.  
- Stack **inherits all properties of `Vector<T>`**, including thread safety.

### **Internal Structure of `Stack<T>`**
```
Bottom → [ A ] [ B ] [ C ] ← Top
```
- **Push(`D`) →** `[ A ] [ B ] [ C ] [ D ]`  
- **Pop() →** `[ A ] [ B ] [ C ]` (removes `D`)  

---

## **4️⃣ How to Create a `Stack<T>`?**  

### **📍 Creating a Stack**
```java
Stack<Integer> stack = new Stack<>();
```
📌 This creates an **empty Stack**.

---

## **5️⃣ Important Methods in `Stack<T>` (with Examples)**  

### **📍 1. `push(E e)` - Add an element to the top**
```java
stack.push(10);
stack.push(20);
stack.push(30);
System.out.println(stack);  // Output: [10, 20, 30]
```

---

### **📍 2. `pop()` - Remove and return the top element**
```java
int topElement = stack.pop();
System.out.println(topElement);  // Output: 30
System.out.println(stack);  // Output: [10, 20]
```

---

### **📍 3. `peek()` - Get the top element without removing it**
```java
int topElement = stack.peek();
System.out.println(topElement);  // Output: 20
System.out.println(stack);  // Output: [10, 20] (unchanged)
```

---

### **📍 4. `isEmpty()` - Check if stack is empty**
```java
System.out.println(stack.isEmpty());  // Output: false
```

---

### **📍 5. `search(E e)` - Find an element’s position from the top**
```java
int position = stack.search(10);
System.out.println(position);  // Output: 2 (position from top, 1-based index)
```
📌 **Returns -1 if element is not found.**

---

### **📍 6. `size()` - Get number of elements in the stack**
```java
System.out.println(stack.size());  // Output: 2
```

---

### **📍 7. `contains(E e)` - Check if an element exists**
```java
System.out.println(stack.contains(20));  // Output: true
System.out.println(stack.contains(40));  // Output: false
```

---

### **📍 8. `clear()` - Remove all elements**
```java
stack.clear();
System.out.println(stack);  // Output: []
```

---

## **6️⃣ Performance of `Stack<T>`**  

| Operation | Time Complexity |
|-----------|---------------|
| `push(E e)` | O(1) |
| `pop()` | O(1) |
| `peek()` | O(1) |
| `search(E e)` | O(n) |
| `isEmpty()` | O(1) |

📌 **Stack operations are generally fast (O(1))**, but searching takes **O(n)** time.

---

## **7️⃣ `Stack<T>` vs `ArrayDeque<T>` (Which is better?)**  

| Feature | `Stack<T>` | `ArrayDeque<T>` |
|---------|------------|----------------|
| **Thread Safe?** | ✅ Yes | ❌ No |
| **Performance** | 🚫 Slower (synchronized) | ✅ Faster (unsynchronized) |
| **LIFO Support** | ✅ Yes | ✅ Yes |
| **Used for?** | Legacy Code, Thread Safety | Better Performance |

🚀 **Use `ArrayDeque<T>` instead of `Stack<T>` for better performance!**  

---

## **📌 Conclusion**
✅ `Stack<T>` is a **LIFO (Last In, First Out) data structure** in Java.  
✅ It is **thread-safe**, but **slower than alternatives like `ArrayDeque<T>`**.  
✅ It is used in **undo/redo, recursion, expression evaluation, etc.**  
✅ **Use `Stack<T>` when you need thread safety, but prefer `ArrayDeque<T>` for better performance.**  

---


# **📌 Deep Dive into `CopyOnWriteArrayList<T>` in Java**  

## **1️⃣ What is `CopyOnWriteArrayList<T>`?**  

🔹 `CopyOnWriteArrayList<T>` is a **thread-safe** version of `ArrayList<T>`.  
🔹 It belongs to the `java.util.concurrent` package.  
🔹 It **allows multiple threads to read the list concurrently without locking**.  
🔹 But, **modifications (add, remove, set) create a new copy of the array**, making it different from `ArrayList<T>`.  
🔹 Best suited for **scenarios where reads are more frequent than writes**.  

---

## **2️⃣ Why Use `CopyOnWriteArrayList<T>`?**  

💡 **When should you use `CopyOnWriteArrayList<T>`?**  

✅ **If multiple threads need to read the list simultaneously**.  
✅ **If reads happen more often than writes** (because writes are costly).  
✅ **If you want to avoid `ConcurrentModificationException`** during iteration.  
✅ **Best for caching, notifications, and event handling systems**.  

🚫 **But...**  
- **Every modification (add, remove) creates a new copy of the list**, which makes it **memory-heavy**.  
- **Slower for frequent modifications** compared to `ArrayList<T>` and `LinkedList<T>`.  

---

## **3️⃣ Internal Working of `CopyOnWriteArrayList<T>`**  

📌 **How does it work?**  
- `CopyOnWriteArrayList<T>` uses **an internal array (`Object[] array`) to store elements**.  
- Every time a modification occurs (add, remove, set), **a new copy of the entire array is created**.  
- This ensures that **read operations are never blocked**, but **modifications are expensive**.  

### **Internal Structure**
```
Original List: [ A ] [ B ] [ C ]
Modification (add D) → New List: [ A ] [ B ] [ C ] [ D ]
```
- **Reads use the old array** until the modification is complete.  
- **After modification, the reference is updated to the new array.**  

---

## **4️⃣ How to Create a `CopyOnWriteArrayList<T>`?**  

📌 **Import the package:**  
```java
import java.util.concurrent.CopyOnWriteArrayList;
```

### **📍 Creating a CopyOnWriteArrayList**
```java
CopyOnWriteArrayList<Integer> list = new CopyOnWriteArrayList<>();
```
📌 This creates an **empty thread-safe list**.

---

## **5️⃣ Important Methods in `CopyOnWriteArrayList<T>` (with Examples)**  

### **📍 1. `add(E e)` - Add an element to the list**
```java
list.add(10);
list.add(20);
list.add(30);
System.out.println(list);  // Output: [10, 20, 30]
```

---

### **📍 2. `remove(int index)` - Remove element at a specific index**
```java
list.remove(1);
System.out.println(list);  // Output: [10, 30]
```

---

### **📍 3. `get(int index)` - Get element at a specific index**
```java
int element = list.get(0);
System.out.println(element);  // Output: 10
```

---

### **📍 4. `size()` - Get number of elements in the list**
```java
System.out.println(list.size());  // Output: 2
```

---

### **📍 5. `contains(E e)` - Check if an element exists**
```java
System.out.println(list.contains(30));  // Output: true
System.out.println(list.contains(50));  // Output: false
```

---

### **📍 6. `set(int index, E e)` - Update an element at a specific index**
```java
list.set(1, 40);
System.out.println(list);  // Output: [10, 40]
```

---

### **📍 7. `iterator()` - Get an iterator (safe from `ConcurrentModificationException`)**
```java
for (Integer num : list) {
    System.out.println(num);
}
```
📌 Unlike `ArrayList<T>`, this **will NOT throw `ConcurrentModificationException`** even if another thread modifies the list while iterating.

---

### **📍 8. `clear()` - Remove all elements**
```java
list.clear();
System.out.println(list);  // Output: []
```

---

## **6️⃣ Performance of `CopyOnWriteArrayList<T>`**  

| Operation | Time Complexity |
|-----------|---------------|
| `add(E e)` | O(n) (creates a new array) |
| `remove(int index)` | O(n) (creates a new array) |
| `get(int index)` | O(1) |
| `contains(E e)` | O(n) |
| `set(int index, E e)` | O(n) (creates a new array) |
| `iterator()` | O(n) (creates a snapshot) |

📌 **Read operations (`get()`) are fast (O(1)), but modifications (`add()`, `set()`, `remove()`) are slow (O(n)).**  

---

## **7️⃣ `CopyOnWriteArrayList<T>` vs `ArrayList<T>` vs `Vector<T>`**  

| Feature | `CopyOnWriteArrayList<T>` | `ArrayList<T>` | `Vector<T>` |
|---------|----------------|-------------|-------------|
| **Thread Safe?** | ✅ Yes | ❌ No | ✅ Yes |
| **Performance (Read)** | ✅ Fast | ✅ Fast | ❌ Slow |
| **Performance (Write)** | 🚫 Slow | ✅ Fast | 🚫 Slow |
| **Best Use Case** | **Many reads, few writes** | **General purpose** | **Legacy multi-threading** |

🚀 **Use `CopyOnWriteArrayList<T>` when multiple threads need fast reads, but few writes.**  

---

## **📌 Conclusion**
✅ `CopyOnWriteArrayList<T>` is a **thread-safe alternative to `ArrayList<T>`**.  
✅ It **allows multiple threads to read safely without locking**.  
✅ **Every modification creates a new copy of the list, making writes expensive**.  
✅ **Best suited for scenarios where reads are more frequent than writes**.  
✅ **Avoid using it when frequent modifications are needed (use `ArrayList<T>` or `ConcurrentLinkedQueue<T>` instead).**  

---

# **📌 Chapter 4: Set Interface (Unique Elements Collection) in Java**  

## **1️⃣ What is a `Set<T>`?**  

📌 **Definition:**  
A `Set<T>` is a collection that **stores unique elements** and does **not allow duplicates**.  

📌 **Key Features of `Set<T>`:**  
✅ **No duplicate elements allowed** (Each element is unique)  
✅ **Can be unordered or ordered** (depends on the implementation)  
✅ **Efficient for search and lookup operations**  
✅ **Useful for mathematical set operations (union, intersection, etc.)**  

---

## **2️⃣ Why Use `Set<T>` Instead of `List<T>`?**  

| Feature | `List<T>` | `Set<T>` |
|---------|----------|----------|
| Allows Duplicates? | ✅ Yes | ❌ No |
| Maintains Order? | ✅ Yes | ❌ (Depends on implementation) |
| Search Performance | ❌ Slower (O(n) for `ArrayList`, O(log n) for `LinkedList`) | ✅ Faster (O(1) in `HashSet`) |
| Best Use Case | **If duplicates are allowed & order matters** | **If you need only unique elements** |

📌 **Use `Set<T>` when you need to store unique elements and don't care about order.**  

---

## **3️⃣ Implementations of `Set<T>` in Java**  

📌 There are **six main implementations** of `Set<T>` in Java:  
### **1️⃣ `HashSet<T>`**
✅ **Unordered**  
✅ Uses **hashing** for fast search operations  
✅ Best for **fast access and uniqueness**  

### **2️⃣ `LinkedHashSet<T>`**
✅ **Maintains insertion order**  
✅ Uses a **linked list + hash table**  
✅ Best for **unique elements while maintaining order**  

### **3️⃣ `TreeSet<T>`**
✅ **Sorted set (Natural ordering)**  
✅ Uses a **Red-Black Tree (Self-balancing BST)**  
✅ Best for **keeping elements sorted**  

### **4️⃣ `EnumSet<T>`**
✅ **Specialized set for Enums**  
✅ **Very fast and memory-efficient**  

### **5️⃣ `ConcurrentSkipListSet<T>`**
✅ **Thread-safe sorted set**  
✅ Uses a **Skip List for ordering**  
✅ Best for **multi-threaded applications**  

### **6️⃣ `CopyOnWriteArraySet<T>`**
✅ **Thread-safe Set**  
✅ **Good for concurrent read-heavy operations**  

---

## **4️⃣ Internal Working of `Set<T>` Implementations**  

📌 **How does `HashSet<T>` store elements?**  
- Uses **a Hash Table (based on HashMap)**.  
- Uses **hashing** to store elements efficiently.  
- **Search, Insert, Delete → O(1) time complexity** (best case).  

📌 **How does `LinkedHashSet<T>` work?**  
- Same as `HashSet<T>`, but **maintains insertion order** using a **doubly linked list**.  

📌 **How does `TreeSet<T>` work?**  
- Uses a **self-balancing Red-Black Tree**.  
- Always **keeps elements sorted**.  
- **Insert, Delete, Search → O(log n) time complexity**.  

📌 **How does `ConcurrentSkipListSet<T>` work?**  
- Uses a **Skip List (multiple linked lists at different levels for fast search)**.  
- **Thread-safe and sorted**.  
- **Slower than `TreeSet` in single-threaded cases but better in multi-threading**.  

---

## **5️⃣ Set Operations (Mathematical Operations on Sets)**  

📌 **Java provides useful methods to perform operations like:**  

### **📍 1. Union (A ∪ B) → Combine elements from both sets**  
```java
Set<Integer> set1 = new HashSet<>(Arrays.asList(1, 2, 3));
Set<Integer> set2 = new HashSet<>(Arrays.asList(3, 4, 5));

set1.addAll(set2);
System.out.println(set1);  // Output: [1, 2, 3, 4, 5]
```

---

### **📍 2. Intersection (A ∩ B) → Common elements**  
```java
Set<Integer> set1 = new HashSet<>(Arrays.asList(1, 2, 3));
Set<Integer> set2 = new HashSet<>(Arrays.asList(3, 4, 5));

set1.retainAll(set2);
System.out.println(set1);  // Output: [3]
```

---

### **📍 3. Difference (A - B) → Elements in A but not in B**  
```java
Set<Integer> set1 = new HashSet<>(Arrays.asList(1, 2, 3));
Set<Integer> set2 = new HashSet<>(Arrays.asList(3, 4, 5));

set1.removeAll(set2);
System.out.println(set1);  // Output: [1, 2]
```

---

### **📍 4. Subset Check (A ⊆ B) → Check if A is a subset of B**  
```java
Set<Integer> set1 = new HashSet<>(Arrays.asList(1, 2));
Set<Integer> set2 = new HashSet<>(Arrays.asList(1, 2, 3, 4, 5));

System.out.println(set2.containsAll(set1));  // Output: true
```

---

## **6️⃣ Choosing the Right `Set<T>` Implementation**  

| Feature | `HashSet<T>` | `LinkedHashSet<T>` | `TreeSet<T>` | `EnumSet<T>` | `ConcurrentSkipListSet<T>` | `CopyOnWriteArraySet<T>` |
|---------|-------------|----------------|------------|------------|---------------------|-------------------|
| **Duplicate Elements** | ❌ No | ❌ No | ❌ No | ❌ No | ❌ No | ❌ No |
| **Maintains Order?** | ❌ No | ✅ Yes (Insertion Order) | ✅ Yes (Sorted) | ❌ No | ✅ Yes (Sorted) | ❌ No |
| **Thread-Safe?** | ❌ No | ❌ No | ❌ No | ❌ No | ✅ Yes | ✅ Yes |
| **Performance** | ✅ Fast | ✅ Fast (Slightly Slower than `HashSet`) | 🚫 Slower | ✅ Fastest for Enums | 🚫 Slower | 🚫 Slowest (Creates Copy on Modification) |
| **Best Use Case** | **General Purpose (Fast)** | **Fast with Order** | **Sorted Data** | **Efficient Enum Handling** | **Thread-Safe Sorted Set** | **Thread-Safe Reads** |

---

## **📌 Conclusion**  
✅ **Use `HashSet<T>` if order doesn’t matter & you want the fastest performance.**  
✅ **Use `LinkedHashSet<T>` if you need insertion order.**  
✅ **Use `TreeSet<T>` if you need sorting.**  
✅ **Use `EnumSet<T>` if you work with Enums.**  
✅ **Use `ConcurrentSkipListSet<T>` if you need thread-safe sorting.**  
✅ **Use `CopyOnWriteArraySet<T>` for thread-safe read-heavy scenarios.**  

---
## **📌 All Methods of Set Interface in Java (Deep Dive)**  

### **1️⃣ Overview of Set<T> Methods**
The `Set<T>` interface in Java is part of the Java Collection Framework and extends the `Collection<T>` interface. Since it represents a unique collection of elements, it provides various methods to **add, remove, check, and manipulate elements efficiently**.  

These methods are **inherited from the Collection Interface** and implemented in classes like `HashSet<T>`, `LinkedHashSet<T>`, `TreeSet<T>`, etc.  

---

## **2️⃣ Methods of the Set Interface**
Here’s a deep dive into **all the important methods** of `Set<T>`, with examples:

### **📍 1. `add(E e)` → Adds an element**
✅ **Adds an element to the set if it is not already present.**  
❌ **If the element already exists, it is ignored.**  
```java
Set<String> set = new HashSet<>();
set.add("Apple");
set.add("Banana");
set.add("Apple"); // Duplicate, won't be added

System.out.println(set); // Output: [Apple, Banana]
```

---

### **📍 2. `addAll(Collection<? extends E> c)` → Adds all elements from another collection**  
✅ **Adds all elements from another collection to the current set.**  
❌ **Duplicate elements are ignored.**
```java
Set<Integer> set1 = new HashSet<>();
set1.add(1);
set1.add(2);

Set<Integer> set2 = new HashSet<>();
set2.add(2);
set2.add(3);

set1.addAll(set2); 
System.out.println(set1); // Output: [1, 2, 3]
```

---

### **📍 3. `remove(Object o)` → Removes an element**
✅ **Removes a specific element from the set.**  
❌ **If the element is not found, nothing happens.**
```java
Set<String> set = new HashSet<>();
set.add("Car");
set.add("Bike");

set.remove("Bike"); 
System.out.println(set); // Output: [Car]
```

---

### **📍 4. `removeAll(Collection<?> c)` → Removes all elements in a given collection**
✅ **Removes all elements from the set that exist in another collection.**
```java
Set<Integer> set = new HashSet<>(Arrays.asList(1, 2, 3, 4, 5));
Set<Integer> removeSet = new HashSet<>(Arrays.asList(2, 4));

set.removeAll(removeSet);
System.out.println(set); // Output: [1, 3, 5]
```

---

### **📍 5. `clear()` → Removes all elements from the set**  
✅ **Empties the set completely.**  
```java
Set<String> set = new HashSet<>(Arrays.asList("A", "B", "C"));
set.clear();

System.out.println(set); // Output: []
```

---

### **📍 6. `contains(Object o)` → Checks if an element exists**
✅ **Returns `true` if the element is in the set, otherwise `false`.**  
```java
Set<String> set = new HashSet<>(Arrays.asList("Apple", "Orange"));
System.out.println(set.contains("Apple"));  // Output: true
System.out.println(set.contains("Banana")); // Output: false
```

---

### **📍 7. `containsAll(Collection<?> c)` → Checks if all elements in a collection exist**
✅ **Returns `true` if the set contains all elements in the given collection.**
```java
Set<Integer> set = new HashSet<>(Arrays.asList(1, 2, 3, 4));
Set<Integer> subSet = new HashSet<>(Arrays.asList(2, 3));

System.out.println(set.containsAll(subSet));  // Output: true
```

---

### **📍 8. `size()` → Returns the number of elements in the set**
✅ **Returns the total number of elements.**
```java
Set<String> set = new HashSet<>(Arrays.asList("A", "B", "C"));
System.out.println(set.size());  // Output: 3
```

---

### **📍 9. `isEmpty()` → Checks if the set is empty**
✅ **Returns `true` if the set contains no elements.**
```java
Set<Integer> set = new HashSet<>();
System.out.println(set.isEmpty());  // Output: true
```

---

### **📍 10. `retainAll(Collection<?> c)` → Keeps only common elements (Intersection)**
✅ **Removes elements that are NOT in the given collection (performs intersection).**
```java
Set<Integer> set = new HashSet<>(Arrays.asList(1, 2, 3, 4, 5));
Set<Integer> commonSet = new HashSet<>(Arrays.asList(2, 4));

set.retainAll(commonSet);
System.out.println(set); // Output: [2, 4]
```

---

### **📍 11. `iterator()` → Returns an iterator to traverse the set**
✅ **Useful for looping through the set elements.**
```java
Set<String> set = new HashSet<>(Arrays.asList("Red", "Blue", "Green"));
Iterator<String> itr = set.iterator();

while (itr.hasNext()) {
    System.out.println(itr.next());
}
```

---

### **📍 12. `toArray()` → Converts the set into an array**
✅ **Returns an array containing all elements in the set.**
```java
Set<String> set = new HashSet<>(Arrays.asList("X", "Y", "Z"));
Object[] arr = set.toArray();

System.out.println(Arrays.toString(arr)); // Output: [X, Y, Z]
```

---

### **📍 13. `toArray(T[] a)` → Converts the set into a typed array**
✅ **Returns an array of type `T` containing all elements.**
```java
Set<String> set = new HashSet<>(Arrays.asList("Java", "Python"));
String[] arr = set.toArray(new String[0]);

System.out.println(Arrays.toString(arr)); // Output: [Java, Python]
```

---

### **📍 14. `equals(Object o)` → Checks if two sets are equal**
✅ **Returns `true` if the sets contain the same elements (order doesn't matter).**
```java
Set<Integer> set1 = new HashSet<>(Arrays.asList(1, 2, 3));
Set<Integer> set2 = new HashSet<>(Arrays.asList(3, 2, 1));

System.out.println(set1.equals(set2)); // Output: true
```

---

### **📍 15. `hashCode()` → Returns the hash code of the set**
✅ **Used for hashing-based storage.**
```java
Set<Integer> set = new HashSet<>(Arrays.asList(10, 20, 30));
System.out.println(set.hashCode()); // Example Output: 32015
```

---

## **3️⃣ Summary of All Methods**
| Method | Description |
|--------|------------|
| `add(E e)` | Adds an element if it's not already present. |
| `addAll(Collection<?> c)` | Adds all elements from another collection. |
| `remove(Object o)` | Removes the specified element. |
| `removeAll(Collection<?> c)` | Removes all elements present in another collection. |
| `clear()` | Removes all elements from the set. |
| `contains(Object o)` | Checks if an element exists in the set. |
| `containsAll(Collection<?> c)` | Checks if all elements of a collection exist. |
| `size()` | Returns the number of elements. |
| `isEmpty()` | Checks if the set is empty. |
| `retainAll(Collection<?> c)` | Keeps only common elements (Intersection). |
| `iterator()` | Returns an iterator to traverse elements. |
| `toArray()` | Converts the set into an object array. |
| `toArray(T[] a)` | Converts the set into a typed array. |
| `equals(Object o)` | Checks if two sets are equal. |
| `hashCode()` | Returns the hash code of the set. |

---

