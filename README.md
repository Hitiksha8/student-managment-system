# student-managment-system
```python
students = []

while True:
    print("\n--- Student Management System ---")
    print("1. Add Student")
    print("2. View Students")
    print("3. Search Student")
    print("4. Delete Student")
    print("5. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        name = input("Enter student name: ")
        age = input("Enter student age: ")
        course = input("Enter course: ")

        students.append({
            "name": name,
            "age": age,
            "course": course
        })

        print("Student added successfully!")

    elif choice == "2":
        if not students:
            print("No students found.")
        else:
            for s in students:
                print(f"Name: {s['name']}, Age: {s['age']}, Course: {s['course']}")

    elif choice == "3":
        name = input("Enter student name: ")

        found = False
        for s in students:
            if s["name"].lower() == name.lower():
                print(f"Name: {s['name']}, Age: {s['age']}, Course: {s['course']}")
                found = True

        if not found:
            print("Student not found.")

    elif choice == "4":
        name = input("Enter student name: ")

        for s in students:
            if s["name"].lower() == name.lower():
                students.remove(s)
                print("Student deleted successfully!")
                break
        else:
            print("Student not found.")

    elif choice == "5":
        print("Thank you!")
        break

    else:
        print("Invalid choice.")
```
1234567
