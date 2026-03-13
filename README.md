# ARRAY IMPLEMENTATION
print("Array Example (Student Marks)")
marks = [85, 90, 78]

marks.append(88)      # insert
marks.remove(78)      # delete

print("Marks:", marks)


# LINKED LIST IMPLEMENTATION
print("\nLinked List Example (Student Marks)")

class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None

    def insert(self, data):
        new = Node(data)
        if not self.head:
            self.head = new
            return
        temp = self.head
        while temp.next:
            temp = temp.next
        temp.next = new

    def display(self):
        temp = self.head
        while temp:
            print(temp.data, end=" -> ")
            temp = temp.next
        print("None")

ll = LinkedList()
ll.insert(85)
ll.insert(90)
ll.insert(78)

ll.display()# Data-structure-practical-program-39
