# Linked List Data Structure in JavaScript 🚀  

A simple implementation of the **Linked List** data structure in JavaScript. This repository demonstrates how to create a linked list class with essential methods and explains its functionality with practical examples.  

---

## What is a Linked List?  
A **Linked List** is a linear data structure where each element (node) contains a reference (link) to the next element in the sequence. Unlike arrays, linked lists do not require contiguous memory locations. They are made up of nodes that store data and a reference to the next node.  

---

## Features  
- **Insert**: Add an item to the linked list.  
- **Delete**: Remove an item from the linked list.  
- **Search**: Find an item in the linked list.  
- **Traverse**: Visit each node in the list.  
- **Size**: Get the number of items in the list.  

---

## Code Implementation  

Here’s the JavaScript implementation of the linked list:  

```javascript
class Node {
    constructor(data) {
        this.data = data; // Data of the node
        this.next = null; // Reference to the next node
    }
}

class LinkedList {
    constructor() {
        this.head = null; // Start of the linked list
        this.size = 0; // Number of elements in the list
    }

    // Insert a new node at the end of the list
    insert(data) {
        const newNode = new Node(data);
        if (this.head === null) {
            this.head = newNode;
        } else {
            let current = this.head;
            while (current.next !== null) {
                current = current.next;
            }
            current.next = newNode;
        }
        this.size++;
    }

    // Delete the first node containing the given data
    delete(data) {
        if (this.head === null) {
            return "List is empty!";
        }
        if (this.head.data === data) {
            this.head = this.head.next;
            this.size--;
            return;
        }
        let current = this.head;
        while (current.next !== null && current.next.data !== data) {
            current = current.next;
        }
        if (current.next === null) {
            return "Data not found!";
        }
        current.next = current.next.next;
        this.size--;
    }

    // Search for a node by its data
    search(data) {
        let current = this.head;
        while (current !== null) {
            if (current.data === data) {
                return true;
            }
            current = current.next;
        }
        return false;
    }

    // Traverse the list and print the data of each node
    traverse() {
        let current = this.head;
        while (current !== null) {
            console.log(current.data);
            current = current.next;
        }
    }
}
```

---

## Example Usage  

```javascript
// Initialize the linked list
const list = new LinkedList();

// Insert items into the list
list.insert("Node 1");
list.insert("Node 2");
list.insert("Node 3");

// Traverse the list
list.traverse(); // Output: Node 1, Node 2, Node 3

// Search for an item
console.log(list.search("Node 2")); // Output: true
console.log(list.search("Node 4")); // Output: false

// Delete an item from the list
list.delete("Node 2");
list.traverse(); // Output: Node 1, Node 3

// Check the size of the list
console.log(list.size); // Output: 2
```

---

## Real-World Applications  
1. **Dynamic Memory Allocation**: Used in operating systems for memory management.  
2. **Database Management**: Linked lists can be used for indexing in databases.  
3. **Implementing Queues and Stacks**: Used in more complex data structures like queues and stacks.  
4. **Navigation Systems**: In systems like file explorers, browsers, etc., to track back and forward navigation.  

---

## TikTok Tutorial 🎥  
Want to see a quick tutorial on how to build this? Check out this TikTok video:  
[]()  

---

## How to Run the Code  
1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/linked-list-data-structure.git
   cd linked-list-data-structure
   ```
2. Open the file `linked-list.js` in your favorite code editor.  
3. Run the file using Node.js:  
   ```bash
   node linked-list.js
   ```

---

## Contributing  
Contributions are welcome! If you have suggestions or want to add new features, feel free to create a pull request.  

---

## License  
This project is licensed under the MIT License.  

---

## Connect with Me:
- [LinkedIn - Vitalii Semianchuk](https://www.linkedin.com/in/vitalii-semianchuk-9812a786/)
- [Telegram - @jsmentorfree](https://t.me/jsmentorfree) - We do a lot of free teaching on this channel! Join us to learn and grow in web development.
- [Tiktok - @jsmentoring](https://www.tiktok.com/@jsmentoring) Everyday new videos
- [Youtube - @jsmentor-uk](https://www.youtube.com/@jsmentor-uk) Mentor live streams
- [Dev.to - fix2015](https://dev.to/fix2015) Javascript featured, live, experience but about Linked List
