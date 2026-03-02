# Library Management System using Lists and Dictionaries

# List to store all books
library = []

# -------- ADD BOOK --------
def add_book():
    print("\n--- Add Book ---")
    book_id = input("Enter Book ID: ")
    title = input("Enter Book Title: ")
    author = input("Enter Author Name: ")

    # Each book is stored as a dictionary
    book = {
        "id": book_id,
        "title": title,
        "author": author,
        "issued": False
    }

    library.append(book)
    print("Book added successfully!\n")


# -------- VIEW BOOKS --------
def view_books():
    print("\n--- View Books ---")

    if not library:
        print("No books in library\n")
        return

    for book in library:
        status = "Issued" if book["issued"] else "Available"
        print("ID:", book["id"])
        print("Title:", book["title"])
        print("Author:", book["author"])
        print("Status:", status)
        print("------------------------")
    print()


# -------- ISSUE BOOK --------
def issue_book():
    print("\n--- Issue Book ---")
    book_id = input("Enter Book ID: ")

    for book in library:
        if book["id"] == book_id:
            if book["issued"]:
                print("Book already issued\n")
            else:
                book["issued"] = True
                print("Book issued successfully\n")
            return

    print("Book not found\n")


# -------- RETURN BOOK --------
def return_book():
    print("\n--- Return Book ---")
    book_id = input("Enter Book ID: ")

    for book in library:
        if book["id"] == book_id:
            if not book["issued"]:
                print("Book was not issued\n")
            else:
                book["issued"] = False
                print("Book returned successfully\n")
            return

    print("Book not found\n")


# -------- SEARCH BOOK --------
def search_book():
    print("\n--- Search Book ---")
    keyword = input("Enter book title: ").lower()

    found = False
    for book in library:
        if keyword in book["title"].lower():
            print("ID:", book["id"])
            print("Title:", book["title"])
            print("Author:", book["author"])
            print("------------------------")
            found = True

    if not found:
        print("No matching book found\n")
    print()


# -------- MAIN MENU --------
while True:
    print("===== LIBRARY MENU =====")
    print("1. Add Book")
    print("2. View Books")
    print("3. Issue Book")
    print("4. Return Book")
    print("5. Search Book")
    print("6. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        add_book()
    elif choice == "2":
        view_books()
    elif choice == "3":
        issue_book()
    elif choice == "4":
        return_book()
    elif choice == "5":
        search_book()
    elif choice == "6":
        print("Program Closed")
        break
    else:
        print("Invalid choice\n")