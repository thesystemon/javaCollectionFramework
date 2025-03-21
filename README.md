

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

# **📌 Deep Dive into `HashSet<T>` in Java (Easy Explanation)**  

## **1️⃣ What is `HashSet<T>`?**
A `HashSet<T>` in Java is a class that implements the `Set<T>` interface and **stores unique elements in an unordered way** using **hashing** for fast retrieval.

✔️ **Stores only unique elements (No duplicates allowed).**  
✔️ **Uses `HashMap` internally for storage.**  
✔️ **Allows `null` values (only one).**  
✔️ **Unordered (No guarantee of insertion order).**  
✔️ **Fast operations (O(1) time complexity for add, remove, contains).**  

---

## **2️⃣ How `HashSet` Works Internally?**
### **🔹 Step 1: Uses `HashMap` for storage**
Internally, `HashSet<T>` uses a `HashMap<T, Object>` where:  
- Each element is stored as **a key** in the `HashMap`.  
- A dummy value (like `PRESENT`) is used as a value.  

```java
private static final Object PRESENT = new Object();
private transient HashMap<E,Object> map;
```

### **🔹 Step 2: Hashing Process**
1. When you **add** an element, it calculates the **hash code** of the element.
2. Finds a suitable **bucket (index)** in the Hash Table.
3. Stores the element **only if it does not already exist.**

### **🔹 Step 3: No Duplicate Elements**
Since `HashMap` does not allow duplicate keys, `HashSet` ensures **no duplicate elements**.

---

## **3️⃣ Creating a `HashSet` (Basic Example)**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        HashSet<String> set = new HashSet<>();

        set.add("Apple");
        set.add("Banana");
        set.add("Mango");
        set.add("Apple"); // Duplicate, will not be added

        System.out.println(set); // Output: [Banana, Apple, Mango] (Unordered)
    }
}
```
- **Duplicates are ignored** (Only one "Apple" is stored).
- **Order is not maintained**.

---

## **4️⃣ Important Methods of `HashSet<T>`**
| Method | Description |
|--------|------------|
| `add(E e)` | Adds an element if it is not already present. |
| `remove(Object o)` | Removes the specified element from the set. |
| `contains(Object o)` | Returns `true` if the element exists. |
| `size()` | Returns the number of elements in the set. |
| `isEmpty()` | Checks if the set is empty. |
| `clear()` | Removes all elements from the set. |
| `iterator()` | Returns an iterator to traverse the set. |

---

## **5️⃣ Detailed Examples of `HashSet<T>` Methods**
### **📍 1. `add(E e)` → Adds an element**
```java
HashSet<Integer> numbers = new HashSet<>();
numbers.add(10);
numbers.add(20);
numbers.add(10); // Duplicate, ignored

System.out.println(numbers); // Output: [20, 10] (Unordered)
```

---

### **📍 2. `remove(Object o)` → Removes an element**
```java
HashSet<String> set = new HashSet<>(Arrays.asList("Java", "Python", "C++"));
set.remove("Python");

System.out.println(set); // Output: [Java, C++]
```

---

### **📍 3. `contains(Object o)` → Checks if an element exists**
```java
HashSet<Integer> numbers = new HashSet<>(Arrays.asList(1, 2, 3));
System.out.println(numbers.contains(2)); // Output: true
System.out.println(numbers.contains(5)); // Output: false
```

---

### **📍 4. `size()` → Returns the total number of elements**
```java
HashSet<String> set = new HashSet<>(Arrays.asList("Apple", "Banana"));
System.out.println(set.size()); // Output: 2
```

---

### **📍 5. `isEmpty()` → Checks if the set is empty**
```java
HashSet<Integer> set = new HashSet<>();
System.out.println(set.isEmpty()); // Output: true
```

---

### **📍 6. `clear()` → Removes all elements**
```java
HashSet<String> set = new HashSet<>(Arrays.asList("A", "B", "C"));
set.clear();

System.out.println(set); // Output: []
```

---

### **📍 7. `iterator()` → Traversing the set**
```java
HashSet<String> set = new HashSet<>(Arrays.asList("Red", "Blue", "Green"));
Iterator<String> itr = set.iterator();

while (itr.hasNext()) {
    System.out.println(itr.next());
}
```
---

## **6️⃣ Performance Analysis**
| Operation | Time Complexity |
|-----------|---------------|
| `add(E e)` | O(1) |
| `remove(Object o)` | O(1) |
| `contains(Object o)` | O(1) |
| `size()` | O(1) |
| `iterator()` | O(n) |

---

## **7️⃣ When to Use `HashSet<T>`?**
| Use `HashSet` When... | Avoid `HashSet` When... |
|------------------|------------------|
| You need **fast lookups**. | You need **ordered elements** (Use `LinkedHashSet`). |
| You don’t care about insertion order. | You need **sorted elements** (Use `TreeSet`). |
| You want to store unique elements. | You need **index-based access** (Use `ArrayList`). |

---

## **8️⃣ Summary**
✔️ **HashSet is a Set implementation that uses hashing to store unique elements.**  
✔️ **Elements are stored in an unordered manner.**  
✔️ **Uses `HashMap` internally for storage.**  
✔️ **Fast operations: O(1) for adding, removing, and searching elements.**  
✔️ **Best choice when you need unique elements and fast access.**

---

# **📌 Deep Dive into `LinkedHashSet<T>` in Java (Easy Explanation)**  

## **1️⃣ What is `LinkedHashSet<T>`?**
A `LinkedHashSet<T>` is a class in Java that implements the `Set<T>` interface and **maintains the insertion order** while ensuring **unique elements**.  

✔️ **Stores only unique elements (No duplicates allowed).**  
✔️ **Maintains insertion order (Unlike `HashSet`).**  
✔️ **Uses a combination of `HashSet` and `LinkedList`.**  
✔️ **Allows `null` values (only one).**  
✔️ **Faster than `TreeSet`, but slightly slower than `HashSet`.**  

---

## **2️⃣ How `LinkedHashSet<T>` Works Internally?**
### **🔹 Step 1: Uses `LinkedHashMap` for storage**
Internally, `LinkedHashSet<T>` uses a **`LinkedHashMap<T, Object>`** where:  
- Each element is stored as **a key** in the `LinkedHashMap`.  
- A dummy value (like `PRESENT`) is used as a value.  

```java
private static final Object PRESENT = new Object();
private transient LinkedHashMap<E,Object> map;
```

### **🔹 Step 2: Maintains Insertion Order**
- Unlike `HashSet`, `LinkedHashSet` **preserves the order in which elements are added**.  
- This happens because `LinkedHashMap` maintains a **doubly linked list** of its entries.  

---

## **3️⃣ Creating a `LinkedHashSet` (Basic Example)**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        LinkedHashSet<String> set = new LinkedHashSet<>();

        set.add("Apple");
        set.add("Banana");
        set.add("Mango");
        set.add("Apple"); // Duplicate, will not be added

        System.out.println(set); // Output: [Apple, Banana, Mango] (Maintains order)
    }
}
```
✔️ **Order is maintained as elements were inserted (`Apple → Banana → Mango`).**  
✔️ **Duplicates are ignored.**  

---

## **4️⃣ Important Methods of `LinkedHashSet<T>`**
| Method | Description |
|--------|------------|
| `add(E e)` | Adds an element if it is not already present. |
| `remove(Object o)` | Removes the specified element from the set. |
| `contains(Object o)` | Returns `true` if the element exists. |
| `size()` | Returns the number of elements in the set. |
| `isEmpty()` | Checks if the set is empty. |
| `clear()` | Removes all elements from the set. |
| `iterator()` | Returns an iterator to traverse the set. |

---

## **5️⃣ Detailed Examples of `LinkedHashSet<T>` Methods**
### **📍 1. `add(E e)` → Adds an element**
```java
LinkedHashSet<Integer> numbers = new LinkedHashSet<>();
numbers.add(10);
numbers.add(20);
numbers.add(10); // Duplicate, ignored

System.out.println(numbers); // Output: [10, 20] (Maintains order)
```

---

### **📍 2. `remove(Object o)` → Removes an element**
```java
LinkedHashSet<String> set = new LinkedHashSet<>(Arrays.asList("Java", "Python", "C++"));
set.remove("Python");

System.out.println(set); // Output: [Java, C++]
```

---

### **📍 3. `contains(Object o)` → Checks if an element exists**
```java
LinkedHashSet<Integer> numbers = new LinkedHashSet<>(Arrays.asList(1, 2, 3));
System.out.println(numbers.contains(2)); // Output: true
System.out.println(numbers.contains(5)); // Output: false
```

---

### **📍 4. `size()` → Returns the total number of elements**
```java
LinkedHashSet<String> set = new LinkedHashSet<>(Arrays.asList("Apple", "Banana"));
System.out.println(set.size()); // Output: 2
```

---

### **📍 5. `isEmpty()` → Checks if the set is empty**
```java
LinkedHashSet<Integer> set = new LinkedHashSet<>();
System.out.println(set.isEmpty()); // Output: true
```

---

### **📍 6. `clear()` → Removes all elements**
```java
LinkedHashSet<String> set = new LinkedHashSet<>(Arrays.asList("A", "B", "C"));
set.clear();

System.out.println(set); // Output: []
```

---

### **📍 7. `iterator()` → Traversing the set**
```java
LinkedHashSet<String> set = new LinkedHashSet<>(Arrays.asList("Red", "Blue", "Green"));
Iterator<String> itr = set.iterator();

while (itr.hasNext()) {
    System.out.println(itr.next());
}
```
---

## **6️⃣ Performance Analysis**
| Operation | Time Complexity |
|-----------|---------------|
| `add(E e)` | O(1) |
| `remove(Object o)` | O(1) |
| `contains(Object o)` | O(1) |
| `size()` | O(1) |
| `iterator()` | O(n) |

---

## **7️⃣ When to Use `LinkedHashSet<T>`?**
| Use `LinkedHashSet` When... | Avoid `LinkedHashSet` When... |
|------------------|------------------|
| You need **fast lookups** with **insertion order maintained**. | You need **sorted elements** (Use `TreeSet`). |
| You want a **unique collection that preserves order**. | You need **index-based access** (Use `ArrayList`). |
| You need moderate performance with predictable order. | You need **higher performance** (Use `HashSet`). |

---

## **8️⃣ Summary**
✔️ **LinkedHashSet is a Set implementation that maintains insertion order.**  
✔️ **Uses `LinkedHashMap` internally to store unique elements.**  
✔️ **Allows fast lookups, insertions, and deletions (O(1) time complexity).**  
✔️ **Best choice when you need unique elements with predictable order.**

---

# **📌 Deep Dive into `TreeSet<T>` in Java (Easy Explanation)**  

## **1️⃣ What is `TreeSet<T>`?**
A `TreeSet<T>` in Java is a class that implements the `NavigableSet<T>` interface and maintains **sorted unique elements**.  

✔️ **Stores only unique elements (No duplicates allowed).**  
✔️ **Maintains elements in sorted (ascending) order.**  
✔️ **Implements `NavigableSet<T>`, which extends `SortedSet<T>`.**  
✔️ **Uses a self-balancing Red-Black Tree for storage.**  
✔️ **Faster than `LinkedList`, but slower than `HashSet`.**  

---

## **2️⃣ How `TreeSet<T>` Works Internally?**
### **🔹 Step 1: Uses a Red-Black Tree**
A **Red-Black Tree** is a type of **self-balancing binary search tree (BST)**.  
Whenever a new element is added:  
- It is first inserted in BST order.  
- If the tree becomes unbalanced, rotations and color changes occur to maintain balance.  
- The height of the tree is maintained as **O(log n)**, ensuring efficient operations.  

### **🔹 Step 2: Maintains Sorted Order**
`TreeSet<T>` sorts elements **automatically in natural order** (`Comparable`) or based on a custom comparator (`Comparator`).  

### **🔹 Step 3: No Duplicates Allowed**
Duplicate elements are ignored while maintaining order.  

---

## **3️⃣ Creating a `TreeSet` (Basic Example)**
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        TreeSet<Integer> numbers = new TreeSet<>();

        numbers.add(50);
        numbers.add(20);
        numbers.add(10);
        numbers.add(40);
        numbers.add(30);
        numbers.add(10); // Duplicate, ignored

        System.out.println(numbers); // Output: [10, 20, 30, 40, 50] (Sorted)
    }
}
```
✔️ **Sorted Order (`10 → 20 → 30 → 40 → 50`)**  
✔️ **Duplicates are ignored.**  

---

## **4️⃣ Important Methods of `TreeSet<T>`**
| Method | Description |
|--------|------------|
| `add(E e)` | Adds an element if it is not already present (sorted). |
| `remove(Object o)` | Removes the specified element from the set. |
| `contains(Object o)` | Returns `true` if the element exists. |
| `size()` | Returns the number of elements in the set. |
| `isEmpty()` | Checks if the set is empty. |
| `clear()` | Removes all elements from the set. |
| `iterator()` | Returns an iterator to traverse the set. |
| `first()` | Returns the smallest (first) element. |
| `last()` | Returns the largest (last) element. |
| `higher(E e)` | Returns the smallest element greater than `e`. |
| `lower(E e)` | Returns the largest element smaller than `e`. |
| `ceiling(E e)` | Returns the smallest element greater than or equal to `e`. |
| `floor(E e)` | Returns the largest element smaller than or equal to `e`. |
| `pollFirst()` | Removes and returns the first element. |
| `pollLast()` | Removes and returns the last element. |

---

## **5️⃣ Detailed Examples of `TreeSet<T>` Methods**
### **📍 1. `add(E e)` → Adds an element**
```java
TreeSet<String> set = new TreeSet<>();
set.add("Banana");
set.add("Apple");
set.add("Mango");

System.out.println(set); // Output: [Apple, Banana, Mango] (Sorted order)
```

---

### **📍 2. `remove(Object o)` → Removes an element**
```java
TreeSet<Integer> numbers = new TreeSet<>(Arrays.asList(10, 20, 30, 40));
numbers.remove(20);

System.out.println(numbers); // Output: [10, 30, 40]
```

---

### **📍 3. `contains(Object o)` → Checks if an element exists**
```java
TreeSet<Integer> numbers = new TreeSet<>(Arrays.asList(5, 10, 15));
System.out.println(numbers.contains(10)); // Output: true
System.out.println(numbers.contains(25)); // Output: false
```

---

### **📍 4. `first()` and `last()` → Get first and last elements**
```java
TreeSet<Integer> numbers = new TreeSet<>(Arrays.asList(100, 50, 75, 25));
System.out.println(numbers.first()); // Output: 25 (Smallest)
System.out.println(numbers.last());  // Output: 100 (Largest)
```

---

### **📍 5. `higher(E e)` and `lower(E e)` → Get next and previous elements**
```java
TreeSet<Integer> numbers = new TreeSet<>(Arrays.asList(10, 20, 30, 40));
System.out.println(numbers.higher(20)); // Output: 30 (Next higher)
System.out.println(numbers.lower(20));  // Output: 10 (Previous lower)
```

---

### **📍 6. `ceiling(E e)` and `floor(E e)` → Get equal or closest values**
```java
TreeSet<Integer> numbers = new TreeSet<>(Arrays.asList(10, 20, 30, 40));
System.out.println(numbers.ceiling(25)); // Output: 30 (Next greater or equal)
System.out.println(numbers.floor(25));   // Output: 20 (Next smaller or equal)
```

---

### **📍 7. `pollFirst()` and `pollLast()` → Remove first and last elements**
```java
TreeSet<Integer> numbers = new TreeSet<>(Arrays.asList(5, 10, 15, 20));
System.out.println(numbers.pollFirst()); // Output: 5 (Removes first)
System.out.println(numbers.pollLast());  // Output: 20 (Removes last)
```

---

### **📍 8. Custom Sorting with `Comparator`**
```java
TreeSet<String> set = new TreeSet<>(Comparator.reverseOrder());
set.add("Banana");
set.add("Apple");
set.add("Mango");

System.out.println(set); // Output: [Mango, Banana, Apple] (Reverse Order)
```

---

## **6️⃣ Performance Analysis**
| Operation | Time Complexity |
|-----------|---------------|
| `add(E e)` | O(log n) |
| `remove(Object o)` | O(log n) |
| `contains(Object o)` | O(log n) |
| `size()` | O(1) |
| `iterator()` | O(n) |

---

## **7️⃣ When to Use `TreeSet<T>`?**
| Use `TreeSet` When... | Avoid `TreeSet` When... |
|------------------|------------------|
| You need elements to be **sorted automatically**. | You need **unordered but fast access** (Use `HashSet`). |
| You want **logarithmic time complexity** (`O(log n)`). | You need **constant time lookups** (`O(1)`, Use `HashSet`). |
| You need efficient **range queries** (`higher(), lower()`). | You need **insertion order to be maintained** (Use `LinkedHashSet`). |

---

## **8️⃣ Summary**
✔️ **TreeSet is a Set implementation that maintains sorted order.**  
✔️ **Uses a self-balancing Red-Black Tree for internal storage.**  
✔️ **Offers `O(log n)` time complexity for insert, delete, and search.**  
✔️ **Best for scenarios where sorted order is required.**

---

# **📌 Deep Dive into `EnumSet<T>` in Java (Easy Explanation)**  

## **1️⃣ What is `EnumSet<T>`?**  
`EnumSet<T>` is a specialized **Set implementation for Enums** in Java. It is designed to work **only with Enums** and is much **faster and memory-efficient** than other Set implementations like `HashSet` or `TreeSet`.  

✔️ **Stores only `enum` values.**  
✔️ **Extremely fast (Better than `HashSet` and `TreeSet`).**  
✔️ **Compact memory usage (Uses bitwise operations).**  
✔️ **Maintains natural order of Enums.**  

---

## **2️⃣ How `EnumSet<T>` Works Internally?**
- Unlike `HashSet`, which uses a **HashMap**, `EnumSet` uses a **bitwise representation** to store elements.  
- Each `enum` constant is assigned a **bit position**, making operations **very fast (`O(1)`)**.  
- Since `EnumSet` is backed by a **bit vector**, it **does not allow null values**.  
- It maintains **insertion order** based on how `enum` constants are declared.  

---

## **3️⃣ Creating an `EnumSet` (Basic Example)**
Let's define an `enum` first:  
```java
enum Days {
    MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY, SUNDAY
}
```
Now, let's create an `EnumSet` and add elements:  
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        EnumSet<Days> weekend = EnumSet.of(Days.SATURDAY, Days.SUNDAY);
        System.out.println(weekend); // Output: [SATURDAY, SUNDAY]
    }
}
```
✔️ **Stores only `enum` values**  
✔️ **Maintains insertion order**  

---

## **4️⃣ Ways to Create an `EnumSet<T>`**
### **📍 1. `EnumSet.of(E... elements)` → Create from specific values**
```java
EnumSet<Days> set = EnumSet.of(Days.MONDAY, Days.WEDNESDAY);
System.out.println(set); // Output: [MONDAY, WEDNESDAY]
```

### **📍 2. `EnumSet.allOf(EnumType.class)` → Create a set of all Enum values**
```java
EnumSet<Days> allDays = EnumSet.allOf(Days.class);
System.out.println(allDays); // Output: [MONDAY, TUESDAY, WEDNESDAY, ...]
```

### **📍 3. `EnumSet.noneOf(EnumType.class)` → Create an empty set**
```java
EnumSet<Days> emptySet = EnumSet.noneOf(Days.class);
System.out.println(emptySet); // Output: []
```

### **📍 4. `EnumSet.range(E from, E to)` → Create a range of Enum values**
```java
EnumSet<Days> midWeek = EnumSet.range(Days.TUESDAY, Days.THURSDAY);
System.out.println(midWeek); // Output: [TUESDAY, WEDNESDAY, THURSDAY]
```

### **📍 5. `EnumSet.copyOf(Collection<E> c)` → Create from another collection**
```java
List<Days> list = Arrays.asList(Days.MONDAY, Days.FRIDAY);
EnumSet<Days> copiedSet = EnumSet.copyOf(list);
System.out.println(copiedSet); // Output: [MONDAY, FRIDAY]
```

---

## **5️⃣ Important Methods of `EnumSet<T>`**
| Method | Description |
|--------|------------|
| `add(E e)` | Adds an element to the set. |
| `remove(E e)` | Removes an element from the set. |
| `contains(E e)` | Checks if the set contains an element. |
| `size()` | Returns the number of elements in the set. |
| `isEmpty()` | Checks if the set is empty. |
| `clear()` | Removes all elements from the set. |
| `iterator()` | Returns an iterator to traverse the set. |
| `complementOf(EnumSet<E> s)` | Returns a set containing all elements **except** those in `s`. |

---

## **6️⃣ Examples of `EnumSet<T>` Methods**
### **📍 1. `add(E e)` and `remove(E e)` → Add & Remove Elements**
```java
EnumSet<Days> set = EnumSet.noneOf(Days.class);
set.add(Days.MONDAY);
set.add(Days.FRIDAY);
set.remove(Days.MONDAY);

System.out.println(set); // Output: [FRIDAY]
```

---

### **📍 2. `contains(E e)` → Check if an element exists**
```java
EnumSet<Days> set = EnumSet.of(Days.WEDNESDAY, Days.FRIDAY);
System.out.println(set.contains(Days.FRIDAY)); // Output: true
System.out.println(set.contains(Days.SUNDAY)); // Output: false
```

---

### **📍 3. `complementOf(EnumSet<E> s)` → Get the complement set**
```java
EnumSet<Days> workingDays = EnumSet.range(Days.MONDAY, Days.FRIDAY);
EnumSet<Days> nonWorkingDays = EnumSet.complementOf(workingDays);

System.out.println(workingDays);  // Output: [MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY]
System.out.println(nonWorkingDays); // Output: [SATURDAY, SUNDAY]
```

---

## **7️⃣ Performance Analysis**
| Operation | Time Complexity |
|-----------|---------------|
| `add(E e)` | O(1) |
| `remove(E e)` | O(1) |
| `contains(E e)` | O(1) |
| `size()` | O(1) |
| `iterator()` | O(n) |

✔️ **Extremely fast because it uses bitwise operations.**  

---

## **8️⃣ When to Use `EnumSet<T>`?**
| Use `EnumSet` When... | Avoid `EnumSet` When... |
|------------------|------------------|
| You have **enum values** to store. | You need to store **non-enum values**. |
| You need a **faster and memory-efficient** Set. | You need to store **null values** (`EnumSet` does not allow `null`). |
| You want **ordered enum storage**. | You need a **hashed or sorted collection** (Use `HashSet` or `TreeSet`). |

---

## **9️⃣ Summary**
✔️ **EnumSet is the best choice for storing Enums in a Set.**  
✔️ **Much faster and memory-efficient than `HashSet` and `TreeSet`.**  
✔️ **Uses bitwise operations for fast access.**  
✔️ **Maintains natural order of Enum constants.**  
✔️ **Does not allow `null` values.**  

---

# **📌 Deep Dive into `ConcurrentSkipListSet<T>` in Java (Easy Explanation)**  

## **1️⃣ What is `ConcurrentSkipListSet<T>`?**  
`ConcurrentSkipListSet<T>` is a **thread-safe, sorted Set implementation** in Java.  
It is part of the **java.util.concurrent** package and is designed for **concurrent (multi-threaded) environments**.  

✔️ **Thread-Safe** (Multiple threads can modify it safely).  
✔️ **Sorted Set** (Maintains natural order of elements).  
✔️ **Non-Synchronized Alternative to `TreeSet`**.  
✔️ **Uses a Skip List (Efficient for concurrent reads/writes).**  
✔️ **Does not allow `null` elements.**  

---

## **2️⃣ How `ConcurrentSkipListSet<T>` Works Internally?**  
- It uses a **Skip List** instead of a Tree or Hash structure.  
- A Skip List is like a **linked list with multiple levels** to speed up searches.  
- It provides **logarithmic time complexity (`O(log n)`) for add, remove, and search** operations.  
- Unlike `TreeSet`, which uses **synchronized locks**, `ConcurrentSkipListSet` allows **lock-free concurrent access**, making it much faster in multi-threaded scenarios.  

🔹 **Comparison with Other Sets**  

| Feature | `ConcurrentSkipListSet` | `TreeSet` | `HashSet` |
|---------|-----------------|---------|---------|
| Thread-Safe? | ✅ Yes | ❌ No | ❌ No |
| Sorted? | ✅ Yes (Natural Order) | ✅ Yes (Natural Order) | ❌ No |
| Performance (Insert/Search) | ⚡ `O(log n)` | ⚡ `O(log n)` | 🔥 `O(1)` |
| Allows `null`? | ❌ No | ❌ No | ✅ Yes |

---

## **3️⃣ Creating a `ConcurrentSkipListSet<T>` (Basic Example)**  
Let's create a `ConcurrentSkipListSet` and add elements to it:  
```java
import java.util.concurrent.*;

public class Main {
    public static void main(String[] args) {
        ConcurrentSkipListSet<Integer> set = new ConcurrentSkipListSet<>();

        set.add(10);
        set.add(5);
        set.add(20);
        set.add(15);

        System.out.println(set); // Output: [5, 10, 15, 20] (Sorted Order)
    }
}
```
✔️ **Elements are always sorted in natural order**.  
✔️ **Thread-Safe operations without explicit locking**.  

---

## **4️⃣ Important Methods of `ConcurrentSkipListSet<T>`**
| Method | Description |
|--------|------------|
| `add(E e)` | Adds an element to the set. |
| `remove(E e)` | Removes an element from the set. |
| `contains(E e)` | Checks if the set contains an element. |
| `size()` | Returns the number of elements in the set. |
| `isEmpty()` | Checks if the set is empty. |
| `pollFirst()` | Retrieves and removes the **smallest** element. |
| `pollLast()` | Retrieves and removes the **largest** element. |
| `headSet(E toElement)` | Returns elements **less than** `toElement`. |
| `tailSet(E fromElement)` | Returns elements **greater than or equal to** `fromElement`. |
| `subSet(E fromElement, E toElement)` | Returns a range of elements. |

---

## **5️⃣ Examples of `ConcurrentSkipListSet<T>` Methods**
### **📍 1. `add(E e)`, `remove(E e)`, and `contains(E e)`**
```java
ConcurrentSkipListSet<Integer> set = new ConcurrentSkipListSet<>();
set.add(10);
set.add(5);
set.add(20);
set.remove(10);

System.out.println(set.contains(10)); // Output: false
System.out.println(set); // Output: [5, 20]
```
✔️ **`add()` inserts elements in sorted order.**  
✔️ **`remove()` deletes elements safely in multi-threaded environments.**  
✔️ **`contains()` checks if an element exists.**  

---

### **📍 2. `pollFirst()` and `pollLast()` → Retrieve & Remove First/Last Element**
```java
ConcurrentSkipListSet<Integer> set = new ConcurrentSkipListSet<>();
set.add(10);
set.add(5);
set.add(20);

System.out.println(set.pollFirst()); // Output: 5 (Removes Smallest Element)
System.out.println(set.pollLast());  // Output: 20 (Removes Largest Element)
System.out.println(set); // Output: [10]
```

---

### **📍 3. `headSet(E toElement)` → Get elements less than a value**
```java
ConcurrentSkipListSet<Integer> set = new ConcurrentSkipListSet<>();
set.add(10);
set.add(5);
set.add(20);
set.add(15);

System.out.println(set.headSet(15)); // Output: [5, 10]
```
✔️ **Returns all elements smaller than `15`**  

---

### **📍 4. `tailSet(E fromElement)` → Get elements greater than or equal to a value**
```java
ConcurrentSkipListSet<Integer> set = new ConcurrentSkipListSet<>();
set.add(10);
set.add(5);
set.add(20);
set.add(15);

System.out.println(set.tailSet(15)); // Output: [15, 20]
```
✔️ **Returns all elements `>= 15`**  

---

### **📍 5. `subSet(E fromElement, E toElement)` → Get a range of elements**
```java
ConcurrentSkipListSet<Integer> set = new ConcurrentSkipListSet<>();
set.add(10);
set.add(5);
set.add(20);
set.add(15);

System.out.println(set.subSet(10, 20)); // Output: [10, 15]
```
✔️ **Returns elements in the range `[10, 20)` (exclusive of 20)**  

---

## **6️⃣ Performance Analysis**
| Operation | Time Complexity |
|-----------|---------------|
| `add(E e)` | `O(log n)` |
| `remove(E e)` | `O(log n)` |
| `contains(E e)` | `O(log n)` |
| `pollFirst() / pollLast()` | `O(log n)` |
| `headSet(E e) / tailSet(E e) / subSet(E e, E e)` | `O(log n)` |

✔️ **Faster than `TreeSet` in concurrent scenarios.**  
✔️ **Performs better in multi-threaded applications.**  

---

## **7️⃣ When to Use `ConcurrentSkipListSet<T>`?**
| Use `ConcurrentSkipListSet` When... | Avoid `ConcurrentSkipListSet` When... |
|--------------------------|--------------------------|
| You need a **thread-safe sorted Set**. | You don't need sorting (Use `ConcurrentHashMap`). |
| You need **fast concurrent reads & writes**. | You need **faster writes** (`HashSet` is faster for single-threaded use). |
| You need **logarithmic time complexity (`O(log n)`)**. | You need constant-time lookups (`HashSet` provides `O(1)`). |

---

## **8️⃣ Summary**
✔️ **Thread-Safe alternative to `TreeSet`**.  
✔️ **Faster concurrent operations than `TreeSet`**.  
✔️ **Uses Skip List for `O(log n)` operations**.  
✔️ **Maintains elements in sorted order**.  
✔️ **Does not allow `null` values**.  

---

Yes! Before moving to `CopyOnWriteArraySet<T>`, let's first understand **SortedSet<T>** in deep detail.  

---

# **📌 Deep Dive into `SortedSet<T>` in Java (Easy Explanation)**  

## **1️⃣ What is `SortedSet<T>`?**  
A **`SortedSet<T>`** is a specialized version of the `Set<T>` interface that **maintains elements in a sorted order**.  
It is part of the **`java.util` package** and is implemented by `TreeSet<T>`.  

✔️ **No Duplicate Elements** (Like `Set<T>`)  
✔️ **Maintains Sorted Order** (Ascending order by default)  
✔️ **Supports Range Queries** (`headSet()`, `tailSet()`, `subSet()`)  
✔️ **Implements `NavigableSet<T>`** (which extends `SortedSet<T>` for more flexibility)  

---

## **2️⃣ How `SortedSet<T>` Works Internally?**  
- It **extends `Set<T>`** and enforces a **sorting order**.  
- It can use **natural ordering (Comparable)** or **custom ordering (Comparator)**.  
- The most common implementation is **`TreeSet<T>`**, which is based on a **Red-Black Tree**.  
- The **sorting mechanism is automatic**, meaning elements are always stored in sorted order.  

---

## **3️⃣ Declaring a `SortedSet<T>` in Java**  
Since `SortedSet<T>` is an interface, we use `TreeSet<T>` as an implementation.  

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        SortedSet<Integer> sortedSet = new TreeSet<>();

        sortedSet.add(30);
        sortedSet.add(10);
        sortedSet.add(20);
        sortedSet.add(50);
        sortedSet.add(40);

        System.out.println(sortedSet); // Output: [10, 20, 30, 40, 50] (Sorted Order)
    }
}
```
✔️ **Automatically maintains sorted order**.  
✔️ **Duplicates are not allowed**.  

---

## **4️⃣ Important Methods of `SortedSet<T>`**
| Method | Description |
|--------|------------|
| `first()` | Returns the first (smallest) element. |
| `last()` | Returns the last (largest) element. |
| `headSet(E toElement)` | Returns elements **less than** `toElement`. |
| `tailSet(E fromElement)` | Returns elements **greater than or equal to** `fromElement`. |
| `subSet(E fromElement, E toElement)` | Returns elements within the range `[fromElement, toElement)`. |
| `comparator()` | Returns the comparator used for ordering (or `null` for natural ordering). |

---

## **5️⃣ Examples of `SortedSet<T>` Methods**
### **📍 1. `first()` and `last()` → Get First and Last Element**
```java
SortedSet<Integer> set = new TreeSet<>();
set.add(10);
set.add(30);
set.add(20);
set.add(50);
set.add(40);

System.out.println(set.first()); // Output: 10
System.out.println(set.last());  // Output: 50
```
✔️ **Retrieves the smallest and largest elements.**  

---

### **📍 2. `headSet(E toElement)` → Get Elements Less Than a Value**
```java
SortedSet<Integer> set = new TreeSet<>();
set.add(10);
set.add(20);
set.add(30);
set.add(40);
set.add(50);

System.out.println(set.headSet(30)); // Output: [10, 20]
```
✔️ **Returns elements smaller than `30`**.  

---

### **📍 3. `tailSet(E fromElement)` → Get Elements Greater Than or Equal to a Value**
```java
SortedSet<Integer> set = new TreeSet<>();
set.add(10);
set.add(20);
set.add(30);
set.add(40);
set.add(50);

System.out.println(set.tailSet(30)); // Output: [30, 40, 50]
```
✔️ **Returns elements `>= 30`**.  

---

### **📍 4. `subSet(E fromElement, E toElement)` → Get a Range of Elements**
```java
SortedSet<Integer> set = new TreeSet<>();
set.add(10);
set.add(20);
set.add(30);
set.add(40);
set.add(50);

System.out.println(set.subSet(20, 40)); // Output: [20, 30]
```
✔️ **Returns elements in the range `[20, 40)` (exclusive of 40)**.  

---

### **📍 5. `comparator()` → Get the Sorting Comparator**
```java
SortedSet<Integer> set = new TreeSet<>();
System.out.println(set.comparator()); // Output: null (Natural Ordering)
```
✔️ **Returns `null` if elements are sorted naturally**.  

---

## **6️⃣ Performance Analysis**
| Operation | Time Complexity |
|-----------|---------------|
| `add(E e)` | `O(log n)` |
| `remove(E e)` | `O(log n)` |
| `contains(E e)` | `O(log n)` |
| `first() / last()` | `O(1)` |
| `headSet(E e) / tailSet(E e) / subSet(E e, E e)` | `O(log n)` |

✔️ **Uses a Red-Black Tree for efficient sorting**.  
✔️ **Faster than `LinkedList` but slower than `HashSet` for insertions/removals**.  

---

## **7️⃣ When to Use `SortedSet<T>`?**
| Use `SortedSet` When... | Avoid `SortedSet` When... |
|------------------------|--------------------------|
| You need **automatically sorted elements**. | You don't care about ordering (Use `HashSet`). |
| You need **range queries** (`headSet()`, `tailSet()`, etc.). | You need **fast lookups (`O(1)`)** (Use `HashSet`). |
| You need **logarithmic time complexity (`O(log n)`)**. | You need **constant-time inserts/deletes (`O(1)`)**. |

---

## **8️⃣ Summary**
✔️ **`SortedSet<T>` maintains sorted order**.  
✔️ **Implemented using `TreeSet<T>` (Red-Black Tree)**.  
✔️ **Supports range queries like `headSet()`, `tailSet()`, `subSet()`**.  
✔️ **Does not allow duplicate elements**.  
✔️ **Faster than `LinkedList`, but slower than `HashSet`**.  

---

# **📌 Deep Dive into `CopyOnWriteArraySet<T>` in Java (Easy Explanation)**  

## **1️⃣ What is `CopyOnWriteArraySet<T>`?**  
A **`CopyOnWriteArraySet<T>`** is a thread-safe implementation of the `Set<T>` interface. It is part of the **`java.util.concurrent`** package and is designed for **concurrent environments** where reads are frequent but writes (modifications) are rare.

✔️ **Thread-Safe** (No need for manual synchronization)  
✔️ **No Duplicate Elements** (Like `Set<T>`)  
✔️ **Based on `CopyOnWriteArrayList<T>`** (Internally uses an array)  
✔️ **Best for Scenarios with Frequent Reads and Rare Writes**  

---

## **2️⃣ How `CopyOnWriteArraySet<T>` Works Internally?**  
- It is backed by a **`CopyOnWriteArrayList<T>`**.  
- Every time a **modification (add/remove) occurs**, it creates a **new copy of the underlying array**.  
- **Iterators are fail-safe**, meaning they do not throw `ConcurrentModificationException`.  
- **Best suited for scenarios where reading happens more frequently than writing**.  

---

## **3️⃣ Declaring a `CopyOnWriteArraySet<T>` in Java**  
Since `CopyOnWriteArraySet<T>` is a concrete class, we can instantiate it directly.

```java
import java.util.concurrent.CopyOnWriteArraySet;

public class Main {
    public static void main(String[] args) {
        CopyOnWriteArraySet<Integer> set = new CopyOnWriteArraySet<>();

        set.add(10);
        set.add(20);
        set.add(30);
        set.add(10); // Duplicate, will not be added

        System.out.println(set); // Output: [10, 20, 30]
    }
}
```
✔️ **Automatically avoids duplicates**.  
✔️ **Thread-safe without explicit locks**.  

---

## **4️⃣ Important Methods of `CopyOnWriteArraySet<T>`**
| Method | Description |
|--------|------------|
| `add(E e)` | Adds an element to the set (if not already present). |
| `remove(E e)` | Removes the element from the set. |
| `contains(E e)` | Checks if an element is present in the set. |
| `size()` | Returns the number of elements in the set. |
| `iterator()` | Returns a fail-safe iterator. |
| `toArray()` | Converts the set into an array. |

---

## **5️⃣ Examples of `CopyOnWriteArraySet<T>` Methods**
### **📍 1. `add()` and `remove()` → Add and Remove Elements**
```java
import java.util.concurrent.CopyOnWriteArraySet;

public class Main {
    public static void main(String[] args) {
        CopyOnWriteArraySet<String> set = new CopyOnWriteArraySet<>();

        set.add("Apple");
        set.add("Banana");
        set.add("Cherry");

        System.out.println(set); // Output: [Apple, Banana, Cherry]

        set.remove("Banana");
        System.out.println(set); // Output: [Apple, Cherry]
    }
}
```
✔️ **Handles duplicates and thread safety automatically**.  

---

### **📍 2. `contains()` → Check If an Element Exists**
```java
CopyOnWriteArraySet<Integer> set = new CopyOnWriteArraySet<>();
set.add(100);
set.add(200);
set.add(300);

System.out.println(set.contains(200)); // Output: true
System.out.println(set.contains(400)); // Output: false
```
✔️ **Efficiently checks for element presence**.  

---

### **📍 3. `iterator()` → Fail-Safe Iterator**
```java
import java.util.concurrent.CopyOnWriteArraySet;
import java.util.Iterator;

public class Main {
    public static void main(String[] args) {
        CopyOnWriteArraySet<String> set = new CopyOnWriteArraySet<>();
        set.add("A");
        set.add("B");
        set.add("C");

        Iterator<String> iterator = set.iterator();
        while (iterator.hasNext()) {
            System.out.println(iterator.next());
            set.add("D"); // No ConcurrentModificationException!
        }

        System.out.println(set); // Output: [A, B, C, D]
    }
}
```
✔️ **Iterator does not throw `ConcurrentModificationException`**.  
✔️ **Changes made while iterating will not affect the current iterator**.  

---

## **6️⃣ Performance Analysis**
| Operation | Time Complexity |
|-----------|---------------|
| `add(E e)` | `O(n)` (Creates a new copy of the array) |
| `remove(E e)` | `O(n)` |
| `contains(E e)` | `O(n)` |
| `iteration` | `O(n)` |

✔️ **Best for multi-threaded environments with frequent reads and rare writes**.  
✔️ **Not suitable for scenarios with frequent insertions/removals (`O(n)`)**.  

---

## **7️⃣ When to Use `CopyOnWriteArraySet<T>`?**
| Use `CopyOnWriteArraySet<T>` When... | Avoid `CopyOnWriteArraySet<T>` When... |
|--------------------------------------|--------------------------------------|
| **Frequent reads, rare writes**. | **Frequent additions/removals** (`O(n)`). |
| **Multiple threads accessing the set**. | **Performance is critical** (Use `HashSet` for faster operations). |
| **You need fail-safe iterators**. | **You have large datasets** (Memory overhead is high). |

---

## **8️⃣ Summary**
✔️ **Thread-safe `Set<T>` implementation** (No need for manual synchronization).  
✔️ **Uses `CopyOnWriteArrayList<T>` internally** (Every modification creates a new copy).  
✔️ **Best for read-heavy operations in multi-threaded environments**.  
✔️ **Fail-safe iterators (No `ConcurrentModificationException`)**.  
✔️ **Not suitable for frequent writes (`O(n)` complexity)**.  

---

# **📌 Chapter 5: Queue Interface (FIFO Data Structure) in Java (Deep and Easy Explanation)**  

---

## **1️⃣ What is a Queue?**
A **Queue** is a **FIFO (First-In-First-Out)** data structure, meaning the **first element added** will be the **first element removed**.

✔️ **Imagine a queue at a movie ticket counter:**  
- The first person who arrives will be the first one to get the ticket.  
- The next person waits in line until it's their turn.  

✔️ **Real-Life Examples of Queues:**  
- **Print Queue:** The first document sent to the printer gets printed first.  
- **Call Center Support:** The first customer in line gets connected to an agent first.  

✔️ **Java Provides `Queue<T>` Interface**  
- It is part of **`java.util` package** and extends the `Collection<T>` interface.  
- **Different Implementations** are available based on requirements.  

---

## **2️⃣ Why Do We Need a Queue in Java?**
🔹 **Problem with Arrays & Lists:**  
- `ArrayList` and `LinkedList` allow insertion and removal, but they do **not follow FIFO automatically**.  
- Using **`remove(0)`** in an `ArrayList` is slow (`O(n)`) because all elements shift left.  

🔹 **Queue is the Solution:**  
- Efficiently **adds elements at the rear** and **removes from the front** (`O(1)`).  
- Provides **built-in methods** for managing elements.  

---

## **3️⃣ Queue Interface and Its Methods**
| Method | Description |
|--------|------------|
| `add(E e)` | Adds an element at the end (throws exception if full). |
| `offer(E e)` | Adds an element at the end (returns false if full). |
| `remove()` | Removes and returns the front element (throws exception if empty). |
| `poll()` | Removes and returns the front element (returns null if empty). |
| `element()` | Retrieves the front element without removing (throws exception if empty). |
| `peek()` | Retrieves the front element without removing (returns null if empty). |

✔️ **Use `offer()` and `poll()` instead of `add()` and `remove()` to avoid exceptions.**  

---

## **4️⃣ Queue Hierarchy in Java**
```
Queue<T>  (Interface)
│
├── LinkedList<T>  (Doubly Linked List Implementation)
│
├── PriorityQueue<T>  (Min-Heap Implementation)
│
├── Deque<T>  (Double-Ended Queue Interface)
│   ├── ArrayDeque<T>  (Array-Based Deque)
│   ├── LinkedList<T>  (Also Implements Deque)
│
├── ConcurrentLinkedQueue<T>  (Thread-Safe, Non-Blocking Queue)
│
├── BlockingQueue<T>  (Used in Multi-Threading)
│   ├── ArrayBlockingQueue<T>
│   ├── LinkedBlockingQueue<T>
│   ├── PriorityBlockingQueue<T>
│   ├── SynchronousQueue<T>
│   ├── DelayQueue<T>
```

---

## **5️⃣ Types of Queue Implementations in Java**
Let's go through the different types of `Queue<T>` implementations.

### **1️⃣ LinkedList<T> as a Queue**
- Implements `Queue<T>`, `Deque<T>`, and `List<T>`.
- Can be used as **FIFO Queue** or **Deque**.
- Not thread-safe.

### **2️⃣ PriorityQueue<T>**
- Uses **Min-Heap** internally.
- Orders elements based on **natural ordering or custom comparator**.
- Does **not** guarantee FIFO.

### **3️⃣ Deque<T> (Double-Ended Queue)**
- Allows insertion and deletion from **both ends**.
- `ArrayDeque<T>` and `LinkedList<T>` implement `Deque<T>`.

### **4️⃣ ArrayDeque<T> (Resizable Array-Based Deque)**
- Faster than `Stack<T>` for LIFO.
- Faster than `LinkedList<T>` for FIFO.

### **5️⃣ ConcurrentLinkedQueue<T>**
- **Thread-safe implementation** of `Queue<T>`.
- **Non-blocking** (uses **CAS** instead of locks).

### **6️⃣ BlockingQueue<T> (Used in Multi-Threading)**
- Designed for **multi-threading scenarios**.
- Blocks producer/consumer threads if the queue is full/empty.
- Common implementations:
  - `ArrayBlockingQueue<T>` → **Fixed-size array-based blocking queue**.
  - `LinkedBlockingQueue<T>` → **Linked list-based blocking queue**.
  - `PriorityBlockingQueue<T>` → **Priority-based blocking queue**.
  - `SynchronousQueue<T>` → **Transfers elements between threads directly**.
  - `DelayQueue<T>` → **Stores elements with delayed processing**.

---

## **6️⃣ Performance Comparison of Queue Implementations**
| Queue Type | Insertion (`O`) | Deletion (`O`) | Thread-Safe? |
|------------|--------------|-------------|--------------|
| `LinkedList<T>` | `O(1)` | `O(1)` | ❌ No |
| `PriorityQueue<T>` | `O(log n)` | `O(log n)` | ❌ No |
| `ArrayDeque<T>` | `O(1)` | `O(1)` | ❌ No |
| `ConcurrentLinkedQueue<T>` | `O(1)` | `O(1)` | ✅ Yes (Non-Blocking) |
| `BlockingQueue<T>` | `O(1)` | `O(1)` | ✅ Yes (Blocking) |

---

## **7️⃣ When to Use Which Queue?**
| **Use Case** | **Best Queue Implementation** |
|-------------|-----------------------------|
| Simple FIFO operations | `LinkedList<T>` |
| Priority-based processing | `PriorityQueue<T>` |
| Double-ended queue operations | `ArrayDeque<T>` |
| Multi-threaded queue (non-blocking) | `ConcurrentLinkedQueue<T>` |
| Multi-threaded queue (blocking) | `BlockingQueue<T>` |

---

## **📌 Summary**
✔️ **Queue<T> follows FIFO (First-In-First-Out).**  
✔️ **Different implementations available:** `LinkedList<T>`, `PriorityQueue<T>`, `ArrayDeque<T>`, `ConcurrentLinkedQueue<T>`, `BlockingQueue<T>`.  
✔️ **Use `offer()` and `poll()` instead of `add()` and `remove()` to avoid exceptions.**  
✔️ **Choose the right queue based on performance needs (thread-safety, ordering, blocking, etc.).**  

---

# **🚀 LinkedList<T> as a Queue (Deep & Easy Explanation)**  

---

## **1️⃣ What is LinkedList<T> as a Queue?**
`LinkedList<T>` is a **doubly linked list** that implements the `Queue<T>` interface.  
It allows **FIFO (First-In-First-Out) operations**, making it a **good choice** for a queue.  

✔️ **Key Features of LinkedList as a Queue:**  
- **Uses Nodes** (Each element points to the next and previous element).  
- **Fast Insertions & Deletions (`O(1)`)** at both ends.  
- **Maintains Order** (Insertion order is preserved).  
- **Allows Null Values.**  
- **Not Thread-Safe** (Needs external synchronization for multi-threading).  

✔️ **Real-Life Example:**  
- **Train Coaches:** The first coach attached is the first to leave the station.  

---

## **2️⃣ How LinkedList<T> Works as a Queue?**
✔️ **Queue Operations:**  
1️⃣ **Enqueue (Add element at the rear)** → `offer(E e)` / `add(E e)`  
2️⃣ **Dequeue (Remove element from the front)** → `poll()` / `remove()`  
3️⃣ **Peek (Retrieve front element without removing)** → `peek()` / `element()`  

📌 **Internal Working:**  
- **Each element is stored in a Node (`Node<E>`)**  
- **Two pointers (`head` and `tail`) keep track of the front & rear.**  
- **Adding is done at `tail`**, removing is done from `head`.**  

```
HEAD → [10] → [20] → [30] → TAIL
```

✔️ **Adding 40 to Queue (`offer(40)`)**  
```
HEAD → [10] → [20] → [30] → [40] → TAIL
```

✔️ **Removing (`poll()`)**  
```
HEAD → [20] → [30] → [40] → TAIL  (10 is removed)
```

---

## **3️⃣ LinkedList<T> Methods for Queue**
| Method | Description |
|--------|------------|
| `add(E e)` | Adds an element to the queue (throws exception if full). |
| `offer(E e)` | Adds an element to the queue (returns `false` if full). |
| `remove()` | Removes the front element (throws exception if empty). |
| `poll()` | Removes the front element (returns `null` if empty). |
| `element()` | Retrieves the front element without removing (throws exception if empty). |
| `peek()` | Retrieves the front element without removing (returns `null` if empty). |

---

## **4️⃣ Implementation of LinkedList<T> as a Queue**
```java
import java.util.LinkedList;
import java.util.Queue;

public class LinkedListQueueExample {
    public static void main(String[] args) {
        // Create a Queue using LinkedList
        Queue<Integer> queue = new LinkedList<>();

        // Adding elements to the queue
        queue.offer(10);
        queue.offer(20);
        queue.offer(30);

        System.out.println("Queue: " + queue); // [10, 20, 30]

        // Peek (front element without removing)
        System.out.println("Front Element: " + queue.peek()); // 10

        // Removing elements
        System.out.println("Removed: " + queue.poll()); // 10
        System.out.println("Queue after removal: " + queue); // [20, 30]

        // Checking if queue is empty
        System.out.println("Is queue empty? " + queue.isEmpty()); // false
    }
}
```

✔️ **Output:**
```
Queue: [10, 20, 30]
Front Element: 10
Removed: 10
Queue after removal: [20, 30]
Is queue empty? false
```

---

## **5️⃣ How LinkedList<T> Works Internally as a Queue**
✔️ **Structure:**  
- **Each element is stored in a `Node<E>`.**  
- **Each Node contains:**  
  - `E data` (Element Value)  
  - `Node<E> next` (Pointer to next node)  
  - `Node<E> prev` (Pointer to previous node)  

✔️ **Internal Representation:**
```
head → [10] ↔ [20] ↔ [30] → tail
```
✔️ **Adding an Element (`offer(40)`)**
```
head → [10] ↔ [20] ↔ [30] ↔ [40] → tail
```
✔️ **Removing an Element (`poll()`)**
```
head → [20] ↔ [30] ↔ [40] → tail
```

---

## **6️⃣ Performance Analysis of LinkedList as a Queue**
| Operation | Complexity (`O`) |
|-----------|----------------|
| `offer(E e)` (Add to rear) | `O(1)` |
| `poll()` (Remove from front) | `O(1)` |
| `peek()` (Retrieve front) | `O(1)` |
| Search | `O(n)` |

✔️ **Why is LinkedList Fast for Queue?**  
- **`O(1)` insertion and deletion at both ends** (No shifting needed).  
- **`O(n)` search** (Not efficient for finding elements).  

---

## **7️⃣ When to Use LinkedList as a Queue?**
✔️ **Use `LinkedList<T>` when:**  
✅ **Fast Insertion & Deletion (`O(1)`) are needed.**  
✅ **You don’t need random access (`O(n)`).**  
✅ **Maintaining insertion order is important.**  
✅ **You need a flexible data structure (Can act as a Queue & Deque).**  

❌ **Don’t use LinkedList<T> when:**  
🚫 **You need frequent searching (`O(n)`).**  
🚫 **Memory consumption is a concern (Each node requires extra pointers).**  

---

## **📌 Summary**
✔️ **`LinkedList<T>` implements `Queue<T>`.**  
✔️ **FIFO operations:** Insert at the tail, remove from the head.  
✔️ **Efficient `O(1)` insertion & deletion, but `O(n)` search.**  
✔️ **Uses `Node<E>` (doubly linked list structure).**  
✔️ **Best for scenarios needing fast insert/remove, but not for random access.**  

---

# **🚀 PriorityQueue<T> (Deep & Easy Explanation)**  

---

## **1️⃣ What is a PriorityQueue<T>?**
A **PriorityQueue<T>** is a special type of queue where **elements are ordered based on priority** rather than insertion order.  
It is based on **Heap Data Structure** (Min-Heap or Max-Heap).  

✔️ **Key Features of PriorityQueue:**  
- **Elements are sorted based on priority (Natural or Custom Comparator).**  
- **By default, it is a Min-Heap (Smallest element at the top).**  
- **Does NOT allow `null` values.**  
- **Not thread-safe** (Use `PriorityBlockingQueue` for multi-threading).  

✔️ **Real-Life Example:**  
- **Hospital Emergency Room:** Patients with serious conditions are treated first.  
- **Dijkstra’s Algorithm:** Used in shortest path finding.  

---

## **2️⃣ How PriorityQueue<T> Works?**
✔️ **Queue Operations:**  
1️⃣ **Enqueue (Add element in the correct position based on priority)** → `offer(E e)` / `add(E e)`  
2️⃣ **Dequeue (Remove element with highest priority)** → `poll()` / `remove()`  
3️⃣ **Peek (Retrieve highest-priority element without removing)** → `peek()` / `element()`  

📌 **Default Behavior:**  
- **Min-Heap (Smallest element first).**  
- **Max-Heap (Largest element first) needs a custom comparator.**  

```
Min-Heap:
PriorityQueue<Integer> pq = new PriorityQueue<>();
pq.offer(30);
pq.offer(10);
pq.offer(20);

Internally Stored:  
[10, 30, 20]   → 10 is the highest priority (Min-Heap)
```

✔️ **Adding 5 to Queue (`offer(5)`)**  
```
[5, 10, 20, 30]   → 5 moves to the top
```

✔️ **Removing (`poll()`)**  
```
[10, 30, 20]   → 5 is removed
```

---

## **3️⃣ PriorityQueue<T> Methods**
| Method | Description |
|--------|------------|
| `add(E e)` | Adds an element to the queue (throws exception if full). |
| `offer(E e)` | Adds an element to the queue (returns `false` if full). |
| `remove()` | Removes the highest-priority element (throws exception if empty). |
| `poll()` | Removes the highest-priority element (returns `null` if empty). |
| `element()` | Retrieves the highest-priority element without removing (throws exception if empty). |
| `peek()` | Retrieves the highest-priority element without removing (returns `null` if empty). |

---

## **4️⃣ Implementation of PriorityQueue<T>**
```java
import java.util.PriorityQueue;

public class PriorityQueueExample {
    public static void main(String[] args) {
        // Create a Min-Heap (default)
        PriorityQueue<Integer> pq = new PriorityQueue<>();

        // Adding elements
        pq.offer(30);
        pq.offer(10);
        pq.offer(20);

        System.out.println("PriorityQueue: " + pq); // Output: [10, 30, 20]

        // Peek (Retrieve highest priority element)
        System.out.println("Top Element: " + pq.peek()); // Output: 10

        // Removing elements
        System.out.println("Removed: " + pq.poll()); // Output: 10
        System.out.println("PriorityQueue after removal: " + pq); // Output: [20, 30]
    }
}
```

✔️ **Output:**
```
PriorityQueue: [10, 30, 20]
Top Element: 10
Removed: 10
PriorityQueue after removal: [20, 30]
```

---

## **5️⃣ How PriorityQueue Works Internally?**
✔️ **Structure:**  
- **Uses a Min-Heap (Binary Heap) internally.**  
- **Heap is stored in an array for efficient retrieval.**  
- **Insertion follows heap properties (smallest at root).**  
- **Removal maintains heap properties (restructure after deletion).**  

✔️ **Internal Representation (Heap Structure)**
```
        10
       /  \
     30    20
```
✔️ **Adding 5 (`offer(5)`)**
```
        5
       /  \
     10    20
    /
  30
```
✔️ **Removing (`poll()`)**
```
        10
       /  \
     30    20
```

---

## **6️⃣ Custom Comparator for Max-Heap (Highest First)**
By default, `PriorityQueue` is a **Min-Heap**. To make it a **Max-Heap**, use a custom comparator.

```java
import java.util.PriorityQueue;
import java.util.Collections;

public class MaxHeapExample {
    public static void main(String[] args) {
        // Max-Heap using Comparator
        PriorityQueue<Integer> maxHeap = new PriorityQueue<>(Collections.reverseOrder());

        maxHeap.offer(30);
        maxHeap.offer(10);
        maxHeap.offer(20);

        System.out.println("Max-Heap PriorityQueue: " + maxHeap); // Output: [30, 10, 20]

        System.out.println("Top Element: " + maxHeap.peek()); // Output: 30
        System.out.println("Removed: " + maxHeap.poll()); // Output: 30
    }
}
```
✔️ **Output:**
```
Max-Heap PriorityQueue: [30, 10, 20]
Top Element: 30
Removed: 30
```

---

## **7️⃣ Performance Analysis of PriorityQueue<T>**
| Operation | Complexity (`O`) |
|-----------|----------------|
| `offer(E e)` (Insertion) | `O(log n)` |
| `poll()` (Remove highest priority) | `O(log n)` |
| `peek()` (Retrieve highest priority) | `O(1)` |

✔️ **Why is PriorityQueue Fast?**  
- **Uses Heap structure (Efficient insertion/removal).**  
- **Heap properties ensure quick access to the highest priority.**  

---

## **8️⃣ When to Use PriorityQueue?**
✔️ **Use `PriorityQueue<T>` when:**  
✅ **You need efficient priority-based retrieval.**  
✅ **You need a Min-Heap (`O(log n)` operations).**  
✅ **You need a Max-Heap (With custom comparator).**  

❌ **Don’t use PriorityQueue when:**  
🚫 **You need FIFO ordering (Use `LinkedList` for Queue).**  
🚫 **You need thread-safety (Use `PriorityBlockingQueue`).**  
🚫 **You need fast random access (`O(n)`).**  

---

## **📌 Summary**
✔️ **`PriorityQueue<T>` orders elements based on priority.**  
✔️ **Min-Heap by default (Smallest element first).**  
✔️ **Supports custom comparator for Max-Heap.**  
✔️ **Operations are `O(log n)`, making it efficient.**  
✔️ **Best for priority-based tasks like scheduling, pathfinding, etc.**  

---

# **🚀 Deque<T> (Double-Ended Queue) - Deep & Easy Explanation**  

---

## **1️⃣ What is a Deque<T>?**  
A **Deque (Double-Ended Queue)** is a special type of queue where **elements can be added or removed from both ends (front & rear).**  

✔️ **Key Features of Deque:**  
- **Supports FIFO & LIFO operations.**  
- **Efficient insertions/removals from both ends.**  
- **Allows `null` values (except in concurrent implementations).**  
- **Faster than `LinkedList` for queue operations.**  
- **Thread-safe versions exist (`ConcurrentLinkedDeque`).**  

✔️ **Real-Life Example:**  
- **Deque in Browsers:** Back & Forward navigation history.  
- **Job Scheduling:** Tasks can be added at the beginning or end.  

---

## **2️⃣ How Deque<T> Works?**
✔️ **Operations on Both Ends:**  
1️⃣ **Add to Front** → `addFirst(E e)` / `offerFirst(E e)`  
2️⃣ **Remove from Front** → `removeFirst()` / `pollFirst()`  
3️⃣ **Add to Rear** → `addLast(E e)` / `offerLast(E e)`  
4️⃣ **Remove from Rear** → `removeLast()` / `pollLast()`  
5️⃣ **Peek (Retrieve without removing)** → `peekFirst()` / `peekLast()`  

✔️ **Deque as a Queue (FIFO)**
```
Front ➝ [1, 2, 3, 4, 5] ➝ Rear
```
✔️ **Deque as a Stack (LIFO)**
```
Top ➝ [1, 2, 3, 4, 5] (Last In First Out)
```

---

## **3️⃣ Deque<T> Methods**
| Method | Description |
|--------|------------|
| `addFirst(E e)` | Adds element at the front (throws exception if full). |
| `offerFirst(E e)` | Adds element at the front (returns `false` if full). |
| `addLast(E e)` | Adds element at the rear (throws exception if full). |
| `offerLast(E e)` | Adds element at the rear (returns `false` if full). |
| `removeFirst()` | Removes the first element (throws exception if empty). |
| `pollFirst()` | Removes the first element (returns `null` if empty). |
| `removeLast()` | Removes the last element (throws exception if empty). |
| `pollLast()` | Removes the last element (returns `null` if empty). |
| `peekFirst()` | Retrieves the first element without removing. |
| `peekLast()` | Retrieves the last element without removing. |

---

## **4️⃣ Implementation of Deque<T>**
```java
import java.util.Deque;
import java.util.LinkedList;

public class DequeExample {
    public static void main(String[] args) {
        // Creating a Deque
        Deque<Integer> deque = new LinkedList<>();

        // Adding elements at both ends
        deque.addFirst(10);
        deque.addLast(20);
        deque.offerFirst(5);
        deque.offerLast(25);

        System.out.println("Deque: " + deque); // Output: [5, 10, 20, 25]

        // Retrieving elements
        System.out.println("First Element: " + deque.peekFirst()); // Output: 5
        System.out.println("Last Element: " + deque.peekLast()); // Output: 25

        // Removing elements from both ends
        System.out.println("Removed First: " + deque.pollFirst()); // Output: 5
        System.out.println("Removed Last: " + deque.pollLast()); // Output: 25

        System.out.println("Deque after removal: " + deque); // Output: [10, 20]
    }
}
```

✔️ **Output:**
```
Deque: [5, 10, 20, 25]
First Element: 5
Last Element: 25
Removed First: 5
Removed Last: 25
Deque after removal: [10, 20]
```

---

## **5️⃣ How Deque Works Internally?**
✔️ **Structure:**  
- **Uses a Doubly Linked List or Resizable Array (ArrayDeque).**  
- **Efficient insertions/removals at both ends (`O(1)`).**  

✔️ **Internal Representation (Doubly Linked List)**
```
 NULL ← [5] ⇄ [10] ⇄ [20] ⇄ [25] → NULL
```
✔️ **Adding 30 at front (`addFirst(30)`)**
```
 NULL ← [30] ⇄ [5] ⇄ [10] ⇄ [20] ⇄ [25] → NULL
```
✔️ **Removing last (`pollLast()`)**
```
 NULL ← [30] ⇄ [5] ⇄ [10] ⇄ [20] → NULL
```

---

## **6️⃣ ArrayDeque<T> (Faster Alternative to LinkedList)**
**ArrayDeque** is an array-based **double-ended queue**, faster than `LinkedList`.  

✔️ **Why Use `ArrayDeque` Instead of `LinkedList`?**  
- **No overhead of node pointers (faster).**  
- **Resizable array grows automatically.**  
- **Faster insertion/removal (`O(1)`).**  

```java
import java.util.ArrayDeque;
import java.util.Deque;

public class ArrayDequeExample {
    public static void main(String[] args) {
        Deque<Integer> arrayDeque = new ArrayDeque<>();

        arrayDeque.addFirst(10);
        arrayDeque.addLast(20);
        arrayDeque.offerFirst(5);
        arrayDeque.offerLast(25);

        System.out.println("ArrayDeque: " + arrayDeque); // Output: [5, 10, 20, 25]
    }
}
```

---

## **7️⃣ Performance Analysis of Deque<T>**
| Operation | LinkedList `O(n)` | ArrayDeque `O(1)` |
|-----------|----------------|----------------|
| `addFirst(E e)` | `O(1)` | `O(1)` |
| `addLast(E e)` | `O(1)` | `O(1)` |
| `removeFirst()` | `O(1)` | `O(1)` |
| `removeLast()` | `O(1)` | `O(1)` |
| `getFirst()` | `O(1)` | `O(1)` |
| `getLast()` | `O(1)` | `O(1)` |

✔️ **`ArrayDeque` is the best choice for Deque operations.**  

---

## **8️⃣ When to Use Deque?**
✔️ **Use `Deque<T>` when:**  
✅ **You need insertion/removal from both ends.**  
✅ **You need a fast, resizable queue.**  
✅ **You need LIFO & FIFO behavior.**  

❌ **Don’t use Deque when:**  
🚫 **You need indexed access (Use `ArrayList`).**  
🚫 **You need thread-safety (Use `ConcurrentLinkedDeque`).**  

---

## **📌 Summary**
✔️ **Deque supports adding/removing from both ends.**  
✔️ **Uses `LinkedList` (Doubly Linked List) or `ArrayDeque` (Resizable Array).**  
✔️ **Faster than `LinkedList` for queue operations.**  
✔️ **Best choice: `ArrayDeque` (Faster than `LinkedList`).**  
✔️ **Operations are `O(1)`, making it efficient.**  

---

# 🚀 **ArrayDeque<T> – Deep Dive & Easy Explanation**  

---

## **1️⃣ What is ArrayDeque<T>?**
An **ArrayDeque (Array Double-Ended Queue)** is a **resizable array-based implementation of Deque**, which allows **efficient insertion and removal of elements from both ends**.  

✔️ **Key Features:**  
- **Faster than `LinkedList<T>` for Deque operations.**  
- **Dynamic resizing (no fixed capacity like an array).**  
- **Does NOT allow `null` elements (unlike `LinkedList`).**  
- **Not thread-safe (use `ConcurrentLinkedDeque` for multi-threading).**  

📌 **Real-Life Example:**  
- **Task Scheduling** – Jobs added at the front or end of the queue.  
- **Undo-Redo Feature** – Last action undone (LIFO), or first action redone (FIFO).  

---

## **2️⃣ How Does ArrayDeque<T> Work?**
📌 **Operations on Both Ends**  
1️⃣ **Add at Front** → `addFirst(E e)` / `offerFirst(E e)`  
2️⃣ **Remove from Front** → `removeFirst()` / `pollFirst()`  
3️⃣ **Add at Rear** → `addLast(E e)` / `offerLast(E e)`  
4️⃣ **Remove from Rear** → `removeLast()` / `pollLast()`  
5️⃣ **Peek (Retrieve without removing)** → `peekFirst()` / `peekLast()`  

✔️ **ArrayDeque as a Queue (FIFO)**
```
Front ➝ [1, 2, 3, 4, 5] ➝ Rear
```
✔️ **ArrayDeque as a Stack (LIFO)**
```
Top ➝ [1, 2, 3, 4, 5] (Last In First Out)
```

---

## **3️⃣ Methods of ArrayDeque<T>**
| Method | Description |
|--------|------------|
| `addFirst(E e)` | Adds an element at the front (throws exception if full). |
| `offerFirst(E e)` | Adds an element at the front (returns `false` if full). |
| `addLast(E e)` | Adds an element at the rear (throws exception if full). |
| `offerLast(E e)` | Adds an element at the rear (returns `false` if full). |
| `removeFirst()` | Removes the first element (throws exception if empty). |
| `pollFirst()` | Removes the first element (returns `null` if empty). |
| `removeLast()` | Removes the last element (throws exception if empty). |
| `pollLast()` | Removes the last element (returns `null` if empty). |
| `peekFirst()` | Retrieves the first element without removing. |
| `peekLast()` | Retrieves the last element without removing. |

---

## **4️⃣ Implementation of ArrayDeque<T>**
```java
import java.util.ArrayDeque;
import java.util.Deque;

public class ArrayDequeExample {
    public static void main(String[] args) {
        // Creating an ArrayDeque
        Deque<Integer> deque = new ArrayDeque<>();

        // Adding elements at both ends
        deque.addFirst(10);
        deque.addLast(20);
        deque.offerFirst(5);
        deque.offerLast(25);

        System.out.println("ArrayDeque: " + deque); // Output: [5, 10, 20, 25]

        // Retrieving elements
        System.out.println("First Element: " + deque.peekFirst()); // Output: 5
        System.out.println("Last Element: " + deque.peekLast()); // Output: 25

        // Removing elements from both ends
        System.out.println("Removed First: " + deque.pollFirst()); // Output: 5
        System.out.println("Removed Last: " + deque.pollLast()); // Output: 25

        System.out.println("ArrayDeque after removal: " + deque); // Output: [10, 20]
    }
}
```

✔️ **Output:**
```
ArrayDeque: [5, 10, 20, 25]
First Element: 5
Last Element: 25
Removed First: 5
Removed Last: 25
ArrayDeque after removal: [10, 20]
```

---

## **5️⃣ How ArrayDeque Works Internally?**
📌 **Structure:**  
- Uses **a dynamically resizable circular array**.  
- **Elements wrap around when reaching array capacity.**  
- **Insertion/removal from both ends is O(1)** because it doesn’t require shifting like `ArrayList`.  

✔️ **Internal Representation (Circular Array)**
```
[ _, _, 10, 20, 30, _, _, _ ]
     ↑   ↑    ↑  
    Front  Elements  Rear
```
✔️ **Adding `40` at front (`addFirst(40)`)**
```
[ _, _, 40, 10, 20, 30, _, _ ]
     ↑   ↑    ↑  
    Front  Elements  Rear
```
✔️ **Removing last (`pollLast()`)**
```
[ _, _, 40, 10, 20, _, _, _ ]
     ↑   ↑    ↑  
    Front  Elements  Rear
```

---

## **6️⃣ Performance Analysis of ArrayDeque<T>**
| Operation | ArrayDeque `O(1)` | LinkedList `O(n)` |
|-----------|----------------|----------------|
| `addFirst(E e)` | `O(1)` | `O(1)` |
| `addLast(E e)` | `O(1)` | `O(1)` |
| `removeFirst()` | `O(1)` | `O(1)` |
| `removeLast()` | `O(1)` | `O(1)` |
| `getFirst()` | `O(1)` | `O(1)` |
| `getLast()` | `O(1)` | `O(1)` |

✔️ **ArrayDeque is the best choice for Deque operations.**  

---

## **7️⃣ When to Use ArrayDeque?**
✔️ **Use `ArrayDeque<T>` when:**  
✅ **You need fast insertion/removal from both ends.**  
✅ **You need a resizable array-backed deque.**  
✅ **You don’t need thread-safety.**  

❌ **Don’t use ArrayDeque when:**  
🚫 **You need indexed access (Use `ArrayList`).**  
🚫 **You need thread-safety (Use `ConcurrentLinkedDeque`).**  

---

## **📌 Summary**
✔️ **ArrayDeque supports adding/removing from both ends.**  
✔️ **Uses a dynamic resizable array (circular buffer).**  
✔️ **Faster than `LinkedList` for queue operations.**  
✔️ **Best choice: `ArrayDeque` (Faster than `LinkedList`).**  
✔️ **Operations are `O(1)`, making it efficient.**  

---

# 🚀 **ConcurrentLinkedQueue<T> – Deep Dive & Easy Explanation**  

---

## **1️⃣ What is ConcurrentLinkedQueue<T>?**
A **ConcurrentLinkedQueue** is a **thread-safe, non-blocking, FIFO (First-In-First-Out) queue** that allows multiple threads to access and modify it **without explicit locking**.  

✔️ **Key Features:**  
- ✅ **Thread-safe** (Multiple threads can modify it safely).  
- ✅ **Non-blocking** (Uses **CAS (Compare-And-Swap) operations** instead of locks).  
- ✅ **FIFO Order** (Elements are processed in order of insertion).  
- ✅ **Does NOT allow `null` elements**.  
- ✅ **Uses a **linked-list** internally (Each element points to the next).  

📌 **Real-Life Example:**  
- **Producer-Consumer Pattern** – Multiple producer threads add tasks, while consumer threads process them.  
- **Multi-threaded Job Queue** – A system where multiple users submit jobs for processing.  

---

## **2️⃣ How Does ConcurrentLinkedQueue<T> Work Internally?**
📌 **Non-blocking Mechanism**  
- Instead of locks (`synchronized` keyword), it uses **atomic operations (CAS - Compare-And-Swap)**.  
- This makes it **faster than blocking queues (`BlockingQueue`) in high-concurrency situations**.  

✔️ **Internal Structure (Linked List Implementation)**  
```
Head ➝ [1] ➝ [2] ➝ [3] ➝ Tail
```
- **New elements are added at the tail.**  
- **Elements are removed from the head.**  
- **Each node contains a reference to the next node.**  

---

## **3️⃣ Methods of ConcurrentLinkedQueue<T>**
| Method | Description |
|--------|------------|
| `add(E e)` | Adds an element at the tail (throws exception if `null`). |
| `offer(E e)` | Adds an element at the tail (returns `false` if `null`). |
| `poll()` | Retrieves and removes the head of the queue (returns `null` if empty). |
| `peek()` | Retrieves but does not remove the head (returns `null` if empty). |
| `size()` | Returns the number of elements (not always accurate in multi-threading). |
| `isEmpty()` | Checks if the queue is empty. |
| `iterator()` | Returns an iterator over the elements (weakly consistent). |

✔️ **Important Notes:**  
- 🚀 `size()` may not be accurate in multi-threading because other threads might modify the queue simultaneously.  
- 🚀 **`poll()` is better than `remove()`** since it doesn’t throw an exception if the queue is empty.  

---

## **4️⃣ Implementation of ConcurrentLinkedQueue<T>**
```java
import java.util.concurrent.ConcurrentLinkedQueue;

public class ConcurrentLinkedQueueExample {
    public static void main(String[] args) {
        // Creating a ConcurrentLinkedQueue
        ConcurrentLinkedQueue<Integer> queue = new ConcurrentLinkedQueue<>();

        // Adding elements
        queue.add(10);
        queue.offer(20);
        queue.offer(30);

        System.out.println("Queue: " + queue); // Output: [10, 20, 30]

        // Retrieving elements
        System.out.println("Head Element (peek): " + queue.peek()); // Output: 10

        // Removing elements
        System.out.println("Removed Element (poll): " + queue.poll()); // Output: 10

        System.out.println("Queue after removal: " + queue); // Output: [20, 30]
    }
}
```

✔️ **Output:**
```
Queue: [10, 20, 30]
Head Element (peek): 10
Removed Element (poll): 10
Queue after removal: [20, 30]
```

---

## **5️⃣ How ConcurrentLinkedQueue Works Internally?**
📌 **Uses Atomic References for Thread-Safety**  
- **Each node contains:**  
  - **Value**
  - **Reference to next node**
- **CAS (Compare-And-Swap) is used to modify nodes without locks.**  

✔️ **Example: Adding Elements**  
```
Head ➝ [10] ➝ [20] ➝ [30] ➝ Tail
```
✔️ **Example: Polling (Removing Head)**  
```
Before poll(): Head ➝ [10] ➝ [20] ➝ [30] ➝ Tail
After poll():  Head ➝ [20] ➝ [30] ➝ Tail
```

📌 **Why CAS (Compare-And-Swap)?**  
Instead of **synchronized locks**, CAS ensures that:  
- **If the reference is still the same (no change by another thread), it updates the value.**  
- **If another thread modified it, retry until successful.**  
- **This makes operations faster and scalable in multi-threading.**  

---

## **6️⃣ Performance Analysis of ConcurrentLinkedQueue<T>**
| Operation | Complexity `O(n)` | Notes |
|-----------|----------------|-------|
| `add(E e)` | `O(1)` | Fast insert at the tail |
| `offer(E e)` | `O(1)` | Fast insert at the tail |
| `poll()` | `O(1)` | Fast removal from head |
| `peek()` | `O(1)` | Constant time retrieval |
| `size()` | `O(n)` | Not always accurate |

✔️ **Why use `ConcurrentLinkedQueue`?**  
- **No locking overhead (`synchronized`).**  
- **Scales better in high-concurrency environments.**  
- **Best for multi-threaded queue processing.**  

---

## **7️⃣ When to Use ConcurrentLinkedQueue?**
✔️ **Use `ConcurrentLinkedQueue<T>` when:**  
✅ **Multiple threads need to access a queue concurrently.**  
✅ **You want a non-blocking, lock-free queue.**  
✅ **Elements should be processed in FIFO order.**  
✅ **Performance is critical in a multi-threaded environment.**  

❌ **Don’t use `ConcurrentLinkedQueue<T>` when:**  
🚫 **You need blocking operations (use `BlockingQueue<T>` instead).**  
🚫 **You require precise `size()` calculation.**  

---

## **📌 Summary**
✔️ **ConcurrentLinkedQueue is a non-blocking, thread-safe queue.**  
✔️ **FIFO order is maintained.**  
✔️ **Uses CAS (Compare-And-Swap) for efficient updates.**  
✔️ **Faster than `BlockingQueue` in high-concurrency situations.**  
✔️ **Best for producer-consumer scenarios in multi-threading.**  

---

