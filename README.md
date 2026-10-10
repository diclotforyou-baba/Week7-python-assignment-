
# PLP Python Week 7 Assignment: Lists
# Name: Diclot Selemani

# ==========================================
# PART A: LIST WARMUP
# ==========================================

print("========== PART A: LIST WARMUP ==========")

fruits = ["mango", "banana", "orange", "apple"]

print("First fruit:", fruits[0])
print("Last fruit:", fruits[-1])

fruits.append("pineapple")
print("After adding a fruit:", fruits)

fruits.remove("banana")
print("After removing a fruit:", fruits)

print("Number of fruits:", len(fruits))


# ==========================================
# PART B: SHOPPING LIST MANAGER
# ==========================================

def shopping_manager():
    shopping_list = []

    print("\n========== PART B: SHOPPING LIST ==========")

    while True:
        print("\nMenu: add / remove / show / done")
        choice = input("Enter your choice: ").strip().lower()

        if choice == "add":
            item = input("Enter item to add: ").strip()

            if item:
                shopping_list.append(item)
                print(item, "added to your list.")
            else:
                print("Item cannot be empty.")

        elif choice == "remove":
            item = input("Enter item to remove: ").strip()

            if item in shopping_list:
                shopping_list.remove(item)
                print(item, "removed from your list.")
            else:
                print("That item is not on your list.")

        elif choice == "show":
            if shopping_list:
                print("\nYour shopping list:")
                for item in shopping_list:
                    print(item)
            else:
                print("Your shopping list is empty.")

        elif choice == "done":
            print("Goodbye! Thank you for using the shopping list.")
            break

        else:
            print("Invalid choice. Please enter add, remove, show, or done.")


# ==========================================
# PART C: LIST REPORT
# ==========================================

def list_report():
    print("\n========== PART C: LIST REPORT ==========")

    items = ["bread", "avocado", "milk", "sweet potatoes", "tea"]

    # Print each item with its number
    number = 1
    for item in items:
        print(str(number) + ". " + item)
        number += 1

    # Count item names with more than 4 letters
    count = 0

    for item in items:
        letters = 0

        for character in item:
            if character != " ":
                letters += 1

        if letters > 4:
            count += 1

    print("Items with more than 4 letters:", count)

    # Find the longest item using a loop comparison
    longest = items[0]

    for item in items:
        if len(item) > len(longest):
            longest = item

    print("Longest item:", longest)


# ==========================================
# RUN THE ASSIGNMENT
# ==========================================

if __name__ == "__main__":
    shopping_manager()
    list_report()
