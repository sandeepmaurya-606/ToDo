tasks = []

while True:
    print("\n1. Add Task")
    print("2. View Tasks")
    print("3. Delete Task")
    print("4. Exit")

    choice = input("Choose option: ")

    if choice == "1":
        task = input("Enter task: ")
        tasks.append(task)
        print("Task added!")

    elif choice == "2":
        if not tasks:
            print("No tasks found.")
        else:
            print("\nYour Tasks:")
            for i, t in enumerate(tasks, 1):
                print(f"{i}. {t}")

    elif choice == "3":
        num = int(input("Enter task number to delete: "))
        if 1 <= num <= len(tasks):
            tasks.pop(num - 1)
            print("Task deleted!")
        else:
            print("Invalid number.")

    elif choice == "4":
        print("Goodbye!")
        break

    else:
        print("Invalid choice, try again.")
