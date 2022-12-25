import tkinter as tk

# Creating a dictionary to store contact details
contact_book = {}

# Window for the application
window = tk.Tk()
window.title("Contact Book")
window.geometry("400x400")
window.configure(bg="purple")

# Function to add a new contact
def add_contact():
    print("\nAdding a new contact\n")
    name = entry1.get()
    address = entry2.get()
    phone_number = entry3.get()
    email = entry4.get()
    contact_book[name] = [address, phone_number, email]

# Function to edit an existing contact
def edit_contact():
    print("\nEditing an existing contact\n")
    name = entry1.get()
    if name in contact_book.keys():
        address = entry2.get()
        phone_number = entry3.get()
        email = entry4.get()
        contact_book[name] = [address, phone_number, email]
    else:
        print("No contact exists with that name.")

# Function to delete an existing contact
def delete_contact():
    print("\nDeleting an existing contact\n")
    name = entry1.get()
    if name in contact_book.keys():
        del contact_book[name]
    else:
        print("No contact exists with that name.")

# Function to list all saved contacts
def list_contacts():
    print("\nListing all contacts\n")
    for name, details in contact_book.items():
        print("Name: " + name)
        print("Address: " + details[0])
        print("Phone Number: " + details[1])
        print("Email Address: " + details[2] + "\n")

# Function to save contact book to a file
def save_contacts():
    print("\nSaving contact book...\n")
    file_name = entry5.get()
    f = open(file_name, "w")
    for name, details in contact_book.items():
        f.write("Name: " + name + "\n")
        f.write("Address: " + details[0] + "\n")
        f.write("Phone Number: " + details[1] + "\n")
        f.write("Email Address: " + details[2] + "\n\n")
    f.close()

# Labels for the text entry boxes
label1 = tk.Label(window, text="Name", font='Helvetica 14 bold', bg='purple', fg='white')
label1.place(x=100, y=50)

label2 = tk.Label(window, text="Address", font='Helvetica 14 bold', bg='purple', fg='white')
label2.place(x=100, y=100)

label3 = tk.Label(window, text="Phone Number", font='Helvetica 14 bold', bg='purple', fg='white')
label3.place(x=100, y=150)

label4 = tk.Label(window, text="Email Address", font='Helvetica 14 bold', bg='purple', fg='white')
label4.place(x=100, y=200)

label5 = tk.Label(window, text="File Name", font='Helvetica 14 bold', bg='purple', fg='white')
label5.place(x=100, y=250)

# Text entry boxes
entry1 = tk.Entry(window, font='Helvetica 14')
entry1.place(x=250, y=50)

entry2 = tk.Entry(window, font='Helvetica 14')
entry2.place(x=250, y=100)

entry3 = tk.Entry(window, font='Helvetica 14')
entry3.place(x=250, y=150)

entry4 = tk.Entry(window, font='Helvetica 14')
entry4.place(x=250, y=200)

entry5 = tk.Entry(window, font='Helvetica 14')
entry5.place(x=250, y=250)

# Buttons for the various functions
add_button = tk.Button(window, text="Add Contact", command=add_contact, font='Helvetica 12 bold', bg='black', fg='white')
add_button.place(x=50, y=320, width=100, height=40)

edit_button = tk.Button(window, text="Edit Contact", command=edit_contact, font='Helvetica 12 bold', bg='black', fg='white')
edit_button.place(x=175, y=320, width=100, height=40)

delete_button = tk.Button(window, text="Delete Contact", command=delete_contact, font='Helvetica 12 bold', bg='black', fg='white')
delete_button.place(x=300, y=320, width=100, height=40)

list_button = tk.Button(window, text="List Contacts", command=list_contacts, font='Helvetica 12 bold', bg='black', fg='white')
list_button.place(x=50, y=380, width=100, height=40)

save_button = tk.Button(window, text="Save Contacts", command=save_contacts, font='Helvetica 12 bold', bg='black', fg='white')
save_button.place(x=175, y=380, width=100, height=40)

# Main loop for tkinter
window.mainloop()
