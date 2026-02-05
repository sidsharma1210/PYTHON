📝 To-Do List Project (Python)

A simple console-based To-Do List application built using basic Python concepts only.
This project is ideal for beginners, interviews, and logic-building practice.

🚀 Features

Add new tasks

View all tasks

Delete tasks by task number

Exit the application safely

🛠️ Technologies Used

Python

Core concepts:

Lists

Loops

Conditional statements

❌ No functions
❌ No file handling
❌ No advanced libraries

🧠 Project Logic

A list stores all tasks

A while loop keeps the menu running

if-elif-else handles user choices

for loop displays tasks with numbering

📄 Source Code
tasks = []

while True:
    print("\n--- TO DO LIST ---")
    print("1. Add Task")
    print("2. View Tasks")
    print("3. Delete Task")
    print("4. Exit")

    choice = int(input("Enter your choice: "))

    if choice == 1:
        task = input("Enter task: ")
        tasks.append(task)
        print("Task added successfully.")

    elif choice == 2:
        if len(tasks) == 0:
            print("No tasks available.")
        else:
            print("\nYour Tasks:")
            for i in range(len(tasks)):
                print(i + 1, ".", tasks[i])

    elif choice == 3:
        if len(tasks) == 0:
            print("No tasks to delete.")
        else:
            num = int(input("Enter task number to delete: "))
            if num >= 1 and num <= len(tasks):
                removed = tasks.pop(num - 1)
                print("Deleted task:", removed)
            else:
                print("Invalid task number.")

    elif choice == 4:
        print("Thank you! Exiting To-Do App.")
        break

    else:
        print("Invalid choice. Please try again.")

👨‍💻 Author

Siddhartha Goswami
Process Analyst | Python Learner | Aspiring Data Analyst
