# Ticketing Queue System
# Simple Python Console Version

queue = []
ticket_number = 1

while True:
    print("\n====== TICKETING QUEUE SYSTEM ======")
    print("1. Get Ticket")
    print("2. Next Customer")
    print("3. View Queue")
    print("4. Exit")

    choice = input("Enter choice: ")

     if choice == "1":
        ticket = f"T{ticket_number:03d}"
        queue.append(ticket)

        print(f"\nYour ticket number is: {ticket}")
        ticket_number += 1

    elif choice == "2":
        if len(queue) == 0:
            print("\nNo customers in queue.")
        else:
            serving = queue.pop(0)
            print(f"\nNow Serving: {serving}")

    elif choice == "3":
        if len(queue) == 0:
            print("\nQueue is empty.")
        else:
            print("\nCurrent Queue:")
            for q in queue:
                print(q)

    elif choice == "4":
        print("\nSystem Closed.")
        break

    else:
        print("\nInvalid choice.")
